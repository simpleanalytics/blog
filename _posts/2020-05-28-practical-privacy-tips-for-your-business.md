---
title: Practical privacy tips for your business
author_slug: adriaan
author: Adriaan van Rossum
---

As the founder of [Simple Analytics](https://simpleanalytics.com), I'm running into privacy issues while building our product. Based on those learnings I would like to show you some practical tips to improve the privacy of your visitors. Some of the tips seem very logical but can be hard to implement. That's why I have provided examples with every tip so you or your team can apply them without doing all the research.

In this post I talk about [third-party services](#third-party-services), [CDN providers](#do-not-give-too-much-power-to-your-cdn-provider), [social widgets](#remove-social-widgets), [being ethical towards your visitors](#dont-trick-your-visitors), [marketing emails](#emails), [storing data](#where-do-you-store-your-data), [PII data](#do-not-log-or-ask-pii-data-when-not-needed), [IP anonymization](#ip-anonymization), [syslog](#filters-in-syslog), and [two-factor authentication](#use-two-factor-authentication).

> Some tips might become a bit technical and if you don't have any technical background, feel free to skip those and forward them to your technical team.

## Third-party services

Most businesses use plenty of other third-party services. They help you with providing a better service to your customers, which is great. But it's hard to know how privacy-friendly these services are. While you might know them all (it's required by the GDPR), you don't know if you can trust them. It's healthy to always think of third-party services as untrustable and use them in your product like that. There are a few ways you can limit their effect on your visitors.

### Load third-party scripts only when needed

Sometimes you need to use external scripts. For example, you could be using a chat service or a payment provider. Solution: Only load those scripts on pages where you use them.

For a chat, it may be load every page but for a payment provider, it certainly wouldn't be the same. Don't include those script on every page.

When using a chat that you use on every page you could get a bit creative. For example, you could have a little button that only loads the external script when you click it.

<details markdown="1">
<summary>Show code example</summary>

```js
var button = document.querySelector(".chat-button");
button.addEventlistner("click", function() {
  var script = document.createElement("script");
  script.onload = function () {
    // Do something with the chat script if needed
  }
  script.src = "https://chat.example.com/script.js";
  document.head.appendChild(script);
}
```

</details>

To check if your site uses third-party scripts you can use the [Request Map Generator](https://requestmap.webperf.tools/) built by [Simon Hearne](https://twitter.com/simonhearne) _(thanks to [Jan Klimo](https://twitter.com/janklimo/status/1203708198907047937))._ For [Simple Analytics](https://simpleanalytics.com) it looks like this:

<img loading="lazy" class="border" style="padding: 1rem; margin: 1rem 0;" src="/images/2020-privacy-tips/requestmap-simpleanalytics.jpg" alt="Third-party scripts of Simple Analytics" />

In the diagram above you only see requests going to servers of [Simple Analytics](https://simpleanalytics.com): `simpleanalytics.com`, `simpleanalyticscdn.com`, and `simpleanalytics.io`. The fat pink circle is [our home page video](https://simpleanalytics.com/) which consumes the most bytes. We also use an external payment provider, but we only load the script when the client clicks on the signup, hence in this image you don't see any external scripts.

Compare that to another SaaS like Intercom:

<img loading="lazy" class="border" style="padding: 1rem; margin: 1rem 0;" src="/images/2020-privacy-tips/requestmap-intercom.jpg" alt="Third-party scripts of Intercom" />

There are many external scripts loaded from all kinds of different domains. I'm not saying this is good or bad, but it's a good practice to double-check if all those external parties are needed. Run the [Request Map Generator](https://requestmap.webperf.tools/) and see what services you don't need.

<blockquote role="alert">
  Remember that all external parties can access the data being displayed on the page. If your visitors are logged in and see critical data, these external parties can see that as well.
</blockquote>

## Do not give too much power to your CDN provider

If you use a CDN you are giving them data about your visitors and the power to load a different script then your visitors' request.

### Subresource Integrity

To prevent your CDN provider tampering with the source of your scripts you can use [Subresource Integrity](https://developer.mozilla.org/en-US/docs/Web/Security/Subresource_Integrity) (SRI; the `integrity` attribute on your scripts). You need to create a hash of the source of the script and include this in the script tag via the `integrity` attribute. To generate the integrity hash you can use [srihash.org](https://www.srihash.org/).

```html
<script src="https://cdn.example.com/script.js" integrity="sha384-..."></script>
```

### Cross origin attribute

The `crossorigin` content attribute on media elements is a CORS settings attribute. This is needed to load scripts from other domains (a CDN domain for example). The `anonymous` keyword means that there will be no exchange of user credentials via cookies and some other data between your website and other domains.

<details markdown="1">
<summary>You specify it like this</summary>

```html
<script
  src="https://cdn.example.com/script.js"
  integrity="sha384-..."
  crossorigin="anonymous"
></script>
```

</details>

### Referrer policy attribute

To prevent them knowing the page your visitors are viewing, you can add the `referrerpolicy` attribute with a `no-referrer` value to your script tags.

<details markdown="1">
<summary>Show code example</summary>

```html
<script
  src="https://cdn.example.com/script.js"
  integrity="sha384-..."
  referrerpolicy="no-referrer"
></script>
```

</details>

Although you are not sending the referrer here, the browser does send the origin header with CORS requests. This means that your CDN provider still gets the domain where your visitors land on. If they record IPs they can track the browsing behavior of your visitors. This can only be solved by choosing a CDN provider that anonymizes the IP addresses. The only CDN provider that currently offers IP anonymization is [BunnyCDN](https://bunnycdn.com/) _(we are not affiliated with BunnyCDN)_.

<details markdown="1">
<summary>If you combine all the above features, the HTML will look similar to this</summary>

```html
<script
  src="https://cdn.example.com/script.js"
  integrity="sha384-..."
  crossorigin="anonymous"
  referrerpolicy="no-referrer"
></script>
```

</details>

If you add scripts dynamically you can specify the above features as properties. The properties are case sensitive.

<details markdown="1">
<summary>Both <code>crossOrigin</code> and <code>referrerPolicy</code> have one capital letter in them</summary>

```js
var script = document.createElement("script");
script.src = "https://cdn.example.com/script.js";
script.integrity = "sha384-...";
script.crossOrigin = "anonymous";
script.referrerPolicy = "no-referrer";
```

</details>

### Content Security Policy

To add another layer of security for the script you load you can use a Content Security Policy (CSP). CSP is an added layer of security that helps to detect and mitigate certain types of attacks (including Cross Site Scripting (XSS) and data injection attacks).

There are a few ways you can create your policy: use a server where browsers automatically report to _(or use a service like [report-uri.com](https://report-uri.com/products/content_security_policy) or [Csper](https://csper.io/) that do that for you)_ or generate a report yourself. There are some tools to help you with creating a report yourself: [Report URI](https://report-uri.com/home/generate) and [cspisawesome.com](https://www.cspisawesome.com/) have a wizard, [4ARMED](https://www.4armed.com/blog/how-to-create-content-security-policy/) and [Csper](https://csper.io/docs/generating-content-security-policy) have a browser extension, and [Mozilla](https://developer.mozilla.org/en-US/docs/Web/HTTP/CSP) has great documentation.

When you created your policy you can either specify it via a `<meta>`-tag or a header.

> Afraid of blocking important assets? Test your CSP by using [Content-Security-Policy-Report-Only](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy-Report-Only) to only report without blocking.

## Remove social widgets

Social media companies have a bad reputation for collecting data from your visitors. There are many plugins and ways to track users. Your visitors don't choose to be tracked by those companies, you do.

> If you are a visitor it's recommended to use an ad blocker like [uBlock Origin](getublock.com). It's a well developed browser extension that removes all trackers and ads from your visits. There is a giant on/off button to disable it for the site you are on. It makes your browsing experience safer.

Your visitors can do something about it themselves, but there will always be people that don't know about this tracking or don't know how to prevent it from happening. That's why the EU came with the [GDPR](https://gdpr.eu/), California with the [CCPA](https://www.oag.ca.gov/privacy/ccpa), Brazil with [LGDP](http://www.planalto.gov.br/ccivil_03/_Ato2015-2018/2018/Lei/L13709.htm), and the UK with [PECR](https://ico.org.uk/for-organisations/guide-to-pecr/).

<img loading="lazy" class="border" style="margin-top: 0;" src="/images/2020-privacy-tips/daria-nepriakhina-all-we-need-is-likes.jpg" alt="">
<p class="caption" markdown="1">
  Photo by [Daria Nepriakhina](https://unsplash.com/@epicantus) on [Unsplash](https://unsplash.com/s/photos/social-media)
</p>

> On 29 July 2019, the Court of Justice of the European Union (the "CJEU") ruled that a company embedding on its website a social plugin, such as a Facebook “Like” button, can be considered a data controller [...] – [fieldfisher.com](https://privacylawblog.fieldfisher.com/2019/cjeu-rules-that-companies-using-social-plugins-are-liable-for-the-collection-and-transmission-of-data)

Although you are not in control of what those platforms behind your widgets do with the data from your customers, you are still responsible for what happens with this data.

### Replace Facebooks share button

When you add a Facebook widget like a share button, Facebook recommends you use their scripts. This is great for them because they can collect more data about your visitors. Luckily they provide another way without the use of any of their scripts.

Here is an example with custom buttons and a simple share link. I highly recommend using link implementation instead of any script implementation.

<section id="privacy-button-links-example">

<h1>Share this website via</h1>

<div>
  <a target="_blank" style="background-color: #1877f2;" rel="noreferrer" referrerpolicy="no-referrer" href="https://www.facebook.com/sharer/sharer.php?u=https%3A%2F%2Fblog.simpleanalytics.com%2Fpractical-privacy-tips-for-your-business%3Futm_source%3Dfacebook&amp;src=sdkpreparse"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="white"> <path d="M9 8h-3v4h3v12h5v-12h3.642l.358-4h-4v-1.667c0-.955.192-1.333 1.115-1.333h2.885v-5h-3.808c-3.596 0-5.192 1.583-5.192 4.615v3.385z" /></svg><span>Facebook</span></a>

<a target="_blank" style="background-color: #1da1f2;" rel="noreferrer" referrerpolicy="no-referrer" href="https://twitter.com/share?url=https%3A%2F%2Fblog.simpleanalytics.com%2Fpractical-privacy-tips-for-your-business%3Futm_source%3Dtwitter&amp;text=Practical%20privacy%20tips%20for%20your%20business%20%40SimpleAnalytic%0A%0A"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="white"> <path d="M24 4.557c-.883.392-1.832.656-2.828.775 1.017-.609 1.798-1.574 2.165-2.724-.951.564-2.005.974-3.127 1.195-.897-.957-2.178-1.555-3.594-1.555-3.179 0-5.515 2.966-4.797 6.045-4.091-.205-7.719-2.165-10.148-5.144-1.29 2.213-.669 5.108 1.523 6.574-.806-.026-1.566-.247-2.229-.616-.054 2.281 1.581 4.415 3.949 4.89-.693.188-1.452.232-2.224.084.626 1.956 2.444 3.379 4.6 3.419-2.07 1.623-4.678 2.348-7.29 2.04 2.179 1.397 4.768 2.212 7.548 2.212 9.142 0 14.307-7.721 13.995-14.646.962-.695 1.797-1.562 2.457-2.549z" /></svg><span>Twitter</span></a>

<a target="_blank" style="background-color: #1ebea5;" rel="noreferrer" referrerpolicy="no-referrer" href="https://api.whatsapp.com/send?text=Practical%20privacy%20tips%20for%20your%20business%0A%0Ahttps%3A%2F%2Fblog.simpleanalytics.com%2Fpractical-privacy-tips-for-your-business%3Futm_source%3Dwhatsapp"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="white"> <path d="M.057 24l1.687-6.163c-1.041-1.804-1.588-3.849-1.587-5.946.003-6.556 5.338-11.891 11.893-11.891 3.181.001 6.167 1.24 8.413 3.488 2.245 2.248 3.481 5.236 3.48 8.414-.003 6.557-5.338 11.892-11.893 11.892-1.99-.001-3.951-.5-5.688-1.448l-6.305 1.654zm6.597-3.807c1.676.995 3.276 1.591 5.392 1.592 5.448 0 9.886-4.434 9.889-9.885.002-5.462-4.415-9.89-9.881-9.892-5.452 0-9.887 4.434-9.889 9.884-.001 2.225.651 3.891 1.746 5.634l-.999 3.648 3.742-.981zm11.387-5.464c-.074-.124-.272-.198-.57-.347-.297-.149-1.758-.868-2.031-.967-.272-.099-.47-.149-.669.149-.198.297-.768.967-.941 1.165-.173.198-.347.223-.644.074-.297-.149-1.255-.462-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.297-.347.446-.521.151-.172.2-.296.3-.495.099-.198.05-.372-.025-.521-.075-.148-.669-1.611-.916-2.206-.242-.579-.487-.501-.669-.51l-.57-.01c-.198 0-.52.074-.792.372s-1.04 1.016-1.04 2.479 1.065 2.876 1.213 3.074c.149.198 2.095 3.2 5.076 4.487.709.306 1.263.489 1.694.626.712.226 1.36.194 1.872.118.571-.085 1.758-.719 2.006-1.413.248-.695.248-1.29.173-1.414z" /></svg><span>WhatsApp</span></a>

<a target="_blank" style="background-color: #2867b2;" rel="noreferrer" referrerpolicy="no-referrer" href="https://www.linkedin.com/sharing/share-offsite/?url=https%3A%2F%2Fblog.simpleanalytics.com%2Fpractical-privacy-tips-for-your-business%3Futm_source%3Dlinkedin"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="white"> <path d="M4.98 3.5c0 1.381-1.11 2.5-2.48 2.5s-2.48-1.119-2.48-2.5c0-1.38 1.11-2.5 2.48-2.5s2.48 1.12 2.48 2.5zm.02 4.5h-5v16h5v-16zm7.982 0h-4.968v16h4.969v-8.399c0-4.67 6.029-5.052 6.029 0v8.399h4.988v-10.131c0-7.88-8.922-7.593-11.018-3.714v-2.155z" /></svg><span>LinkedIn</span></a>

</div>
</section>

<style>
section#privacy-button-links-example {
  display: flex;
  flex-direction: column;
  width: 100%;
  background-color: #d7e4f4;
  border: 1px solid #CCDCE6;
  align-items: center;
  justify-content: center;
  padding: 3rem 1rem;
  margin: 0 0 1rem;
}
section#privacy-button-links-example div {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-wrap: wrap;
}
section#privacy-button-links-example h1 {
  font-size: 30px;
  text-align: center;
}
section#privacy-button-links-example a {
  background-color: grey;
  border: 0 solid #e2e8f0;
  border-image: none 100% 1 0 stretch;
  border-radius: .25rem;
  color: #fff;
  display: inline-block;
  margin: .5rem;
  padding: .75rem;
  text-decoration: none;
  font-family: "Space Grotesk", Arial, sans-serif;
  white-space: nowrap;
}
section#privacy-button-links-example svg {
  border: 0 solid #e2e8f0;
  border-image: none 100% 1 0 stretch;
  display: inline-block;
  height: auto;
  margin: -.25rem .5rem 0 0;
  max-width: 100%;
  vertical-align: middle;
}
section#privacy-button-links-example span {
  border: 0 solid #e2e8f0;
  border-image: none 100% 1 0 stretch;
  display: inline;
  margin: 0;
}
</style>

<details markdown="1">
<summary>HTML for above buttons</summary>

Make sure to add `rel="noopener"` or `rel="noreferrer"` [to prevent other pages](https://web.dev/external-anchors-use-rel-noopener/) accessing your window object with the window.opener property. This may allow the other page to redirect your page to a malicious URL. It's called [reverse tabnabbing](https://duckduckgo.com/?q=reverse+tabnabbing).

```html
<section id="privacy-button-links-example">
  <h1>Share this website via</h1>

  <div>
    <a
      target="_blank"
      style="background-color: #1877f2;"
      rel="noreferrer"
      referrerpolicy="no-referrer"
      href="https://www.facebook.com/sharer/sharer.php?u=https%3A%2F%2Fblog.simpleanalytics.com%2Fpractical-privacy-tips-for-your-business%3Futm_source%3Dfacebook&amp;src=sdkpreparse"
      ><svg
        xmlns="http://www.w3.org/2000/svg"
        width="24"
        height="24"
        viewBox="0 0 24 24"
        fill="white"
      >
        <path
          d="M9 8h-3v4h3v12h5v-12h3.642l.358-4h-4v-1.667c0-.955.192-1.333 1.115-1.333h2.885v-5h-3.808c-3.596 0-5.192 1.583-5.192 4.615v3.385z"
        /></svg
      ><span>Facebook</span></a
    >

    <a
      target="_blank"
      style="background-color: #1da1f2;"
      rel="noreferrer"
      referrerpolicy="no-referrer"
      href="https://twitter.com/share?url=https%3A%2F%2Fblog.simpleanalytics.com%2Fpractical-privacy-tips-for-your-business%3Futm_source%3Dtwitter&amp;text=Practical%20privacy%20tips%20for%20your%20business%20%40SimpleAnalytic%0A%0A"
      ><svg
        xmlns="http://www.w3.org/2000/svg"
        width="24"
        height="24"
        viewBox="0 0 24 24"
        fill="white"
      >
        <path
          d="M24 4.557c-.883.392-1.832.656-2.828.775 1.017-.609 1.798-1.574 2.165-2.724-.951.564-2.005.974-3.127 1.195-.897-.957-2.178-1.555-3.594-1.555-3.179 0-5.515 2.966-4.797 6.045-4.091-.205-7.719-2.165-10.148-5.144-1.29 2.213-.669 5.108 1.523 6.574-.806-.026-1.566-.247-2.229-.616-.054 2.281 1.581 4.415 3.949 4.89-.693.188-1.452.232-2.224.084.626 1.956 2.444 3.379 4.6 3.419-2.07 1.623-4.678 2.348-7.29 2.04 2.179 1.397 4.768 2.212 7.548 2.212 9.142 0 14.307-7.721 13.995-14.646.962-.695 1.797-1.562 2.457-2.549z"
        /></svg
      ><span>Twitter</span></a
    >

    <a
      target="_blank"
      style="background-color: #1ebea5;"
      rel="noreferrer"
      referrerpolicy="no-referrer"
      href="https://api.whatsapp.com/send?text=Practical%20privacy%20tips%20for%20your%20business%0A%0Ahttps%3A%2F%2Fblog.simpleanalytics.com%2Fpractical-privacy-tips-for-your-business%3Futm_source%3Dwhatsapp"
      ><svg
        xmlns="http://www.w3.org/2000/svg"
        width="24"
        height="24"
        viewBox="0 0 24 24"
        fill="white"
      >
        <path
          d="M.057 24l1.687-6.163c-1.041-1.804-1.588-3.849-1.587-5.946.003-6.556 5.338-11.891 11.893-11.891 3.181.001 6.167 1.24 8.413 3.488 2.245 2.248 3.481 5.236 3.48 8.414-.003 6.557-5.338 11.892-11.893 11.892-1.99-.001-3.951-.5-5.688-1.448l-6.305 1.654zm6.597-3.807c1.676.995 3.276 1.591 5.392 1.592 5.448 0 9.886-4.434 9.889-9.885.002-5.462-4.415-9.89-9.881-9.892-5.452 0-9.887 4.434-9.889 9.884-.001 2.225.651 3.891 1.746 5.634l-.999 3.648 3.742-.981zm11.387-5.464c-.074-.124-.272-.198-.57-.347-.297-.149-1.758-.868-2.031-.967-.272-.099-.47-.149-.669.149-.198.297-.768.967-.941 1.165-.173.198-.347.223-.644.074-.297-.149-1.255-.462-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.297-.347.446-.521.151-.172.2-.296.3-.495.099-.198.05-.372-.025-.521-.075-.148-.669-1.611-.916-2.206-.242-.579-.487-.501-.669-.51l-.57-.01c-.198 0-.52.074-.792.372s-1.04 1.016-1.04 2.479 1.065 2.876 1.213 3.074c.149.198 2.095 3.2 5.076 4.487.709.306 1.263.489 1.694.626.712.226 1.36.194 1.872.118.571-.085 1.758-.719 2.006-1.413.248-.695.248-1.29.173-1.414z"
        /></svg
      ><span>WhatsApp</span></a
    >

    <a
      target="_blank"
      style="background-color: #2867b2;"
      rel="noreferrer"
      referrerpolicy="no-referrer"
      href="https://www.linkedin.com/sharing/share-offsite/?url=https%3A%2F%2Fblog.simpleanalytics.com%2Fpractical-privacy-tips-for-your-business%3Futm_source%3Dlinkedin"
      ><svg
        xmlns="http://www.w3.org/2000/svg"
        width="24"
        height="24"
        viewBox="0 0 24 24"
        fill="white"
      >
        <path
          d="M4.98 3.5c0 1.381-1.11 2.5-2.48 2.5s-2.48-1.119-2.48-2.5c0-1.38 1.11-2.5 2.48-2.5s2.48 1.12 2.48 2.5zm.02 4.5h-5v16h5v-16zm7.982 0h-4.968v16h4.969v-8.399c0-4.67 6.029-5.052 6.029 0v8.399h4.988v-10.131c0-7.88-8.922-7.593-11.018-3.714v-2.155z"
        /></svg
      ><span>LinkedIn</span></a
    >
  </div>
</section>
```

</details>

<details markdown="1">
<summary>CSS for above buttons</summary>

```css
section#privacy-button-links-example {
  display: flex;
  flex-direction: column;
  width: 100%;
  background-color: #d7e4f4;
  border: 1px solid #ccdce6;
  align-items: center;
  justify-content: center;
  padding: 3rem 1rem;
  margin: 0 0 1rem;
}
section#privacy-button-links-example div {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-wrap: wrap;
}
section#privacy-button-links-example h1 {
  font-size: 30px;
  text-align: center;
}
section#privacy-button-links-example a {
  border: 0 solid #e2e8f0;
  border-image: none 100% 1 0 stretch;
  border-radius: 0.25rem;
  color: #fff;
  display: inline-block;
  margin: 0.5rem;
  padding: 0.75rem;
  text-decoration: none;
  white-space: nowrap;
}
section#privacy-button-links-example svg {
  border: 0 solid #e2e8f0;
  border-image: none 100% 1 0 stretch;
  display: inline-block;
  height: auto;
  margin: -0.25rem 0.5rem 0 0;
  max-width: 100%;
  vertical-align: middle;
}
section#privacy-button-links-example span {
  border: 0 solid #e2e8f0;
  border-image: none 100% 1 0 stretch;
  display: inline;
  margin: 0;
}
```

</details>

The link implementation is a simple link that opens [the Facebook share page](https://www.facebook.com/sharer/sharer.php?u=https%3A%2F%2Fsimpleanalytics.com%2F%3Futm_source%3Dfacebook&src=sdkpreparse) for your visitors. You can put the link behind a button or text link on your website.

<details markdown="1">
<summary>Link implementation explained for nontechnical people</summary>

Let's say you need this link for Facebook:

```
https://www.facebook.com/sharer/sharer.php?u=https%3A%2F%2Fexample.com%2F%3Futm_source%3Dfacebook&src=sdkpreparse
```

You see a lot of weird characters in that URL (link). That's because the link is URL encoded. Use [urlencoder.io](https://www.urlencoder.io/) to easily URL encode your website:

<a href="https://www.urlencoder.io/">
  <img loading="lazy" class="border" style="margin: 1rem auto; width: 500px;" src="/images/2020-privacy-tips/url-encode-online.gif" alt="URL encode online" />
</a>

Prefix the output of [urlencoder.io](https://www.urlencoder.io/) with `https://www.facebook.com/sharer/sharer.php?u=` and append `&src=sdkpreparse` behind it and you have your Facebook share link. Without the tracking and privacy-invasive data collection. You can now share this link with your developers of use it in the CMS of your marketing website.

</details>

### Twitter embedded tweets

On the internet you see the Twitter widget being used a lot. But is it nessessary to send the data from your visitors to Twitter when they just want to see a tweet? A screenshot works just fine:

<a href="https://twitter.com/SimpleAnalytic/status/1262318675283128322">
  <img loading="lazy" class="border" style="margin: 1rem auto; width: 450px;" src="/images/2020-privacy-tips/twitter-embed.jpg" alt="Embedded tweet" />
</a>

## Don't trick your visitors

Tricking your visitors into doing something they don't want to do is bad, and you shouldn't do it. Sometimes it's great to open your website and follow your flow like a new customer. Be aware of things that are not clear and all the popups you see.

### Cookie banners

When browsing the internet you will find many examples of websites trying to trick you in an opt-in for allowing to track you.

For example the home page of the New York Times. When you see a cross (X) you normally would close a dialog box without agreeing to what's being asked. The New York Times just sees it the same as "I agree":

<img loading="lazy" style="margin: 0 auto;" class="border" src="/images/2020-privacy-tips/new-york-times-cookie-banner.jpg" alt="New York Times cookie banner" />

Please don't do this.

## Emails

It's related to don't trick your visitors, but I want to spend a separate section about emails alone.

### Marketing emails

If you have a business, there is a great value by using the email address of your customers. Use it wisely to inform them about new features, help them get around your tool, etc. It's a perk for your business. But if you're sending marketing emails to your customers, be sure they want to be subscribed. You can ask during signup if it's okay for you to send them emails about your tool/service, or you ask if they are okay with you sending some setup guides or tips. Be aware that if you specify how you are going to use their email, and make sure you only use their email for that purpose.

### Email tracking

It's harder to disable email tracking than enabling it. That's why most marketing emails contain trackers. Open rate is considered inaccurate because of client disabling images:

> [...] an email is only counted as 'opened' if the recipient also receives the images embedded in that message, and a large percentage of your email users likely have image-blocking enabled on their email client. [...] – [blog.hubspot.com](https://blog.hubspot.com/blog/tabid/6307/bid/29510/Your-Complete-Guide-to-Measuring-Email-Marketing-Success.aspx)

### Email images

When an image-heavy email doesn't fully download and is viewed by the user, it could end up rendering like this for the subscriber:

<a href="https://twitter.com/flcarneiro/status/568116082835361792">
  <img loading="lazy" class="border" style="margin-top: 1rem; width: 500px;" src="/images/2020-privacy-tips/tweet-embedded-images.jpg" alt="Embedded tweet" />
</a>
<p class="caption" style="text-align: center;" markdown="1">
  [Tweet](https://twitter.com/flcarneiro/status/568116082835361792) found on a blog by [Litmus](https://www.litmus.com/blog/the-ultimate-guide-to-email-image-blocking/)
</p>

When adding images to your emails and not embedding those images in the emails they can look very ugly. More and more email services will stop displaying email trackers and thus images as well. The new [HEY.com](https://hey.com) service [blocks](https://www.businessinsider.com/basecamp-new-email-service-hey-gmail-2020-2?international=true&r=US&IR=T) the so-called tracking pixels. I guess that more will follow.

With [Simple Analytics](https://simpleanalytics.com) we love to share weekly and monthly [email reports](https://docs.simpleanalytics.com/email-reports). When customers have enabled it we send them an email with all images embedded. No trackers or any remote images. No need to connect with anything outside their email client. Give back their privacy: they deserve it!

<a href="https://docs.simpleanalytics.com/email-reports">
  <img loading="lazy" class="border" style="margin-top: 1rem; width: 500px;" src="/images/2020-privacy-tips/email-report.png" alt="Embedded tweet" />
</a>
<p class="caption" style="text-align: center;" markdown="1">
  [Email reports feature](https://docs.simpleanalytics.com/email-reports) of [Simple Analytics](https://simpleanalytics.com)
</p>

### How to keep a good reputation

Another thing with marketing emails is the unsubscribe header. Make sure you have the header set up as it improves your email reputation. The headers could look like this:

```
List-Unsubscribe: <https://example.com/unsub/?uuid=14b2-b2a1>, <mailto:unsubscribe@example.com>
```

In a lot of email clients, the unsubscribe link is placed close to the spam button. You want people to unsubscribe instead of hitting the spam button to prevent damaging your reputation.

## Where do you store your data

It's important to store your data in a country that protects the privacy of its people and the people outside of the country. With [Simple Analytics](https://simpleanalytics.com) we moved our servers to Iceland when we figured that was the best country privacy-wise. According to Freedom House Internet Freedom Scores [Iceland](https://freedomhouse.org/country/iceland/freedom-net/2019) is still the best option:

<a href="https://freedomhouse.org/countries/freedom-net/scores?sort=desc&order=Total%20Score%20and%20Status">
<img loading="lazy" class="border" style="margin: 0; padding: 1rem 1rem 0;" src="/images/2020-privacy-tips/freedomhouse-score.jpg" alt="Freedom House Internet Freedom Scores" /></a>

We later realized Iceland was not the best option provider-wise.

<details markdown="1">
<summary>Here is why</summary>

1. The [Icelandic Modern Media Initiative](https://en.wikipedia.org/wiki/International_Modern_Media_Institute#History) was adopted by parliament but didn’t make it into law (so it’s not the internet freedom haven we thought it was).
1. Our provider claimed to be the largest in Iceland but it was not as mature as bigger providers in Europe, which risked the security of our servers and infrastructure.
1. They had downtime twice this year.
1. The internet cables to Iceland are rather slow. Although it’s geographically ideal — located between North America and Europe — in practice, The Netherlands is a faster location for both.
1. We don't want to move to Switzerland because it would be a marketing move only. The EU provides better privacy laws than Switzerland.
1. We need to move anyway because our current provider does not offer the powerful servers we need.
1. The second-biggest provider in Iceland is legally headquartered in Hong Kong, which is not a preferred location we want to store our data.

> Copied from [our docs page on locations](https://docs.simpleanalytics.com/locations).

</details>

We asked our customers if they would be okay with the move from Iceland to The Netherlands and everybody who voted agreed with our decision.

Be aware of where you put the data from your visitors. Do some research into the hosting provider you are using and the country where it's hosted. Don't pick the cheapest option without knowing why it's cheap.

## Do not log or ask PII data when it's not needed

Personally identifiable information (PII) is information that, when used alone or with other relevant data, can identify an individual. It still happens quite frequently where websites or apps ask you to provide personal details which they don't even need.

### Don't ask full names...

...Unless you really need it. Let people decide for themselves to add their full name. Just ask for a first name if you want to address people in your marketing emails, but don't ask for a full name.

> For people reading that are tired of coming up with fake names: there are [plenty of services out there](https://duckduckgo.com/?q=fake+name+generator) to help create a fake name.

### IP anonymization

This part is rather technical so bear with me. If you are a manager please forward this to your developers. IP anonymization is the most logical thing to do on your servers when talking about privacy. Yet, there are not that many examples of how to do it. A lot of the processes (applications) on your servers log data. For example, _NGINX_ logs data about every request that comes in by default (it's customizable, however). This is great for debugging but it's less good for the privacy of your users. With _NGNIX_ you can't format the error logs so it will always error in the same format. This is very privacy-unfriendly because it contains the full IP address of the user and usually the User-Agent (which can contain unclear identifiers when using the Facebook app).

> You can probably guess a few of the elements of this Facebook User-Agent suffix but it's not all clear to me: `[FBAN/FBIOS;FBAV/221.0.0.0.0;FBBV/154514034;FBDV/iPhone9,4;FBMD/iPhone;FBSN/iOS;FBSV/12.3.0;FBSS/3;FBCR/Siminn;FBID/phone;FBLC/en_GB;FBOP/5;FBRV/155138002]` It does not look like they are tracking their users via the User-Agent suffix, but they tamper with the User-Agent, at least.

### Filters in syslog

[Simple Analytics](https://simpleanalytics.com) uses _NGINX_ which in our case logs to _rsyslog_, often referred to as _syslog_. _rsyslog_ is ofter included in Linux distributions ([official website](https://www.rsyslog.com/)). Luckily _rsyslog_ comes with a great module that's called _mmanon_. This module can be used to filter IP addresses for both v4 and v6 from _rsyslog_ [version 7.3.7](https://www.rsyslog.com/doc/v8-stable/configuration/modules/mmanon.html).

<details markdown="1">
<summary>How to implement anonymization with rsyslog</summary>

On your sever you can check which version of _rsyslog_ you have by running `rsyslogd -v`.

You can enable IP anonymization by adding the following lines to your _rsyslog_ config file. The config file usually lives in `/etc/rsyslog.conf` or `/etc/rsyslog.d/50-default.conf`.

```bash
module(load="mmanon")
action(type="mmanon" mode="zero" ipv4.bits="32" ipv6.bits="128")
```

After you have changed this file make sure to restart _rsyslog_ with `service rsyslog restart`.

#### Next level syslog

If you want to go indepth you can set up some advanced filters to remove sensitive data within your log files or log services.

You could create a syslog config file in `/etc/syslog/...`. I created a file called `/etc/rsyslog.d/30-anonymize.conf` containing:

```sh
# Specify a custom format to anonymize your logs
$template anonymize,"%$year%-%$month%-%$day% %timegenerated:12:19:date-rfc3339% %app-name% %$!new%\n"

# This makes the template the default for all logs
$ActionFileDefaultTemplate anonymize

set $!new = $msg;

# Replace user agents
if re_match($msg,'(Mozilla\\/[0-9]\\.[0-9] [^"\']+)')
then {
  set $!ext = re_extract($msg,'(Mozilla\\/[0-9]\\.[0-9] [^"\']+)',0,1,"");
  set $!new = replace($msg, $!ext, "*** (user agent)");
}
```

</details>

You can do way more, [in our config](https://gist.github.com/adriaanvanrossum/e692b0399f0ca8ab15005315ab0dd694) we hide IPs, credit cards, and user agents.

### Use two-factor authentication

This one is more security-related than privacy, but it's important either way.

If you want to secure the data of your users and prevent others from accessing their data, use a two-factor authentication system. [Don't use SMS](https://duckduckgo.com/?q=sms+two-factor+authentication). Use [TOTP](https://en.wikipedia.org/wiki/Time-based_One-time_Password_algorithm) (Time-based One-time Password) which has lots of apps and integrations. It does not require internet connectivity and can be installed on multiple devices.

### Conclusion

While working on [Simple Analytics](https://simpleanalytics.com), I'm constantly fighting the status quo by finding privacy-friendly ways of handling visitor data. There are way too few guidelines on how to prevent tracking in your own business.

<blockquote role="alert" class="hn" markdown="1">
[Read the discussion](https://news.ycombinator.com/item?id=23337822) on Hacker News
</blockquote>

I hope this post makes the web a bit more privacy-friendly. [Please let me know](https://github.com/simpleanalytics/blog/issues/new) which tips I should add.
