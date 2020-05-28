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

To prevent your CDN provider tempering with the source of your scripts you can use [Subresource Integrity](https://developer.mozilla.org/en-US/docs/Web/Security/Subresource_Integrity) (SRI; the `integrity` attribute on your scripts). You need to create a hash of the source of the script and include this in the script tag via the `integrity` attribute. To generate the integrity hash you can use [srihash.org](https://www.srihash.org/).

```html
<script src="https://cdn.example.com/script.js" integrity="sha384-..."></script>
```

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

To prevent giving the page your visitors are viewing, you can add the `referrerpolicy` attribute with a `no-referrer` value to your script tags.

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

## Remove social widgets

Social media companies do not have a very good reputation for collecting data from your visitors. There are many plugins and ways to track users. Your visitors don't choose to be tracked by those companies, you do.

> If you are a visitor it's recommended to use an ad blocker like [uBlock Origin](getublock.com). It's a well develop browser extension that removes all trackers and ads from your visits. There is a giant on/off button to disable it for the site you are on. It makes your browsing experience safer.

Your visitors can do something about it themselves, but there will always be people that don't know about this tracking or don't know how to prevent it from happening. That's why the EU came with the [GDPR](https://gdpr.eu/), California with the [CCPA](https://www.oag.ca.gov/privacy/ccpa), Brazil with [LGDP](http://www.planalto.gov.br/ccivil_03/_Ato2015-2018/2018/Lei/L13709.htm), and the UK with [PECR](https://ico.org.uk/for-organisations/guide-to-pecr/).

<img loading="lazy" class="border" style="margin-top: 0;" src="/images/2020-privacy-tips/daria-nepriakhina-all-we-need-is-likes.jpg" alt="">
<p class="caption" markdown="1">
  Photo by [Daria Nepriakhina](https://unsplash.com/@epicantus) on [Unsplash](https://unsplash.com/s/photos/social-media)
</p>

> On 29 July 2019, the Court of Justice of the European Union (the "CJEU") ruled that a company embedding on its website a social plugin, such as a Facebook “Like” button, can be considered a data controller [...] – [fieldfisher.com](https://privacylawblog.fieldfisher.com/2019/cjeu-rules-that-companies-using-social-plugins-are-liable-for-the-collection-and-transmission-of-data)

Although you are not in control of what those platforms behind your widgets do with the data from your customers, you are still responsible for what happens with this data.

### Replace Facebooks share button

When you add a Facebook widget like a share button, Facebook recommends you use their third-party scripts. This is great for them because they can collect more data about your visitors. Luckily they provide another way without the use of any scripts.

Here is an example with custom buttons and a simple share link. I highly recommend using link implementation instead of any script implementation.

<img loading="lazy" class="border" style="margin: 1rem auto;" src="/images/2020-privacy-tips/share-buttons.jpg" alt="Custom social media share buttons" />

<details markdown="1">
<summary>Link implementation explained</summary>

The link implementation is a simple link that opens [the Facebook share page](https://www.facebook.com/sharer/sharer.php?u=https%3A%2F%2Fsimpleanalytics.com%2F%3Futm_source%3Dfacebook&src=sdkpreparse) for your visitors. You can put the link behind a button or text link on your website. For example:

```
https://www.facebook.com/sharer/sharer.php?u=https%3A%2F%2Fexample.com%2F%3Futm_source%3Dfacebook&src=sdkpreparse
```

You see a lot of weird characters in that URL (link). That's because the link is URL encoded. Use [urlencoder.io](https://www.urlencoder.io/) to easily URL encode your website:

<a href="https://www.urlencoder.io/">
  <img loading="lazy" class="border" style="margin: 1rem auto; width: 500px;" src="/images/2020-privacy-tips/url-encode-online.gif" alt="URL encode online" />
</a>

Prefix the output of [urlencoder.io](https://www.urlencoder.io/) with `https://www.facebook.com/sharer/sharer.php?u=` and append `&src=sdkpreparse` behind it and you have your Facebook share link. Without the tracking and privacy-invasive data collection.

</details>

### Twitter embedded tweets

On the internet you see the Twitter widget being used a lot. But is it needed to send the data from your visitors to Twitter when they just want to see a tweet? A screenshot works just fine:

<a href="https://twitter.com/SimpleAnalytic/status/1262318675283128322">
  <img loading="lazy" class="border" style="margin: 1rem auto; width: 450px;" src="/images/2020-privacy-tips/twitter-embed.jpg" alt="Embedded tweet" />
</a>

## Don't trick your visitors

Tricking your visitors into doing something they don't want to do. Sometimes it's great to open your website and follow your flow like a new customer. Be aware of things that are not clear and all the popups you see.

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

With [Simple Analytics](https://simpleanalytics.com) we love to share weekly and monthly [email reports](https://docs.simpleanalytics.com/email-reports). When customers have enabled it we send them an email with all images embedded. No trackers or any remote images. No need to connect with anything outside their email client. Give them their privacy back that they deserve.

<a href="https://docs.simpleanalytics.com/email-reports">
  <img loading="lazy" class="border" style="margin-top: 1rem; width: 500px;" src="/images/2020-privacy-tips/email-report.png" alt="Embedded tweet" />
</a>
<p class="caption" style="text-align: center;" markdown="1">
  [Email reports feature](https://docs.simpleanalytics.com/email-reports) of [Simple Analytics](https://simpleanalytics.com)
</p>

### How to keep a good reputation

Another thing with marketing emails is the unsubscribe header. Make sure you have the header setup as it improves your email reputation. The headers could look like this:

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

## Do not log or ask PII data when not needed

It still happens you need to enter personal details for a website or app that does not need it.

### Don't ask full names

Unless you really need it. Let people decide for themselves to add their full name. Just ask for a first name if you want to address people in your marketing emails, but don't ask for a full name.

> For people reading that are tired of coming up with fake names: there are [plenty of services out there](https://duckduckgo.com/?q=fake+name+generator) to help create a fake name.

### IP anonymization

This part is rather technical so bear with me. If you are a manager please forward this to your developers. IP anonymization is the most logical thing to do on your servers when talking about privacy. Yet, there are not that many examples of how to do it. A lot of processes on your servers log data. For example, _NGINX_ logs data about every request (it's customizable) that comes in. This is great for debugging but it's less good for the privacy of your users. With _NGNIX_ you can't format the error logs so it will always error in the same format. This is very privacy-unfriendly because it contains the full IP address of the user and usually the User-Agent (which can contain unclear identifiers when using the Facebook app).

> You can probably guess a few of the elements of this Facebook User-Agent suffix but it's not all clear to me: `[FBAN/FBIOS;FBAV/221.0.0.0.0;FBBV/154514034;FBDV/iPhone9,4;FBMD/iPhone;FBSN/iOS;FBSV/12.3.0;FBSS/3;FBCR/Siminn;FBID/phone;FBLC/en_GB;FBOP/5;FBRV/155138002]` It does not look like they are tracking their users via the User-Agent suffix, but they temper with the User-Agent at least.

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

I hope this post makes the web a bit more privacy-friendly. [Please let me know](https://github.com/simpleanalytics/blog/issues/new) which tips I should add.
