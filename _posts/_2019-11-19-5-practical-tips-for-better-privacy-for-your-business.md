---
title: Practical privacy tips for your business
author_slug: adriaan
author: Adriaan van Rossum
---

As the founder of Simple Analytics I'm running into privacy issue while building our product. Based on those learnings I would like to show you some practical tips to improve the privacy for your visitors. Some of the tips seem very logical but they can be hard to implement. That's why I have provided examples with every tip so you or your team can apply them without doing all the research.

## Third-party services

It's hard to know how privacy friendly third-party are. While you might know them all (it's required by the GDPR), you don't know if you can trust them. It healty to think of third-party services as untrustable and use them in your product like that. There are a few ways you can limit their effect on your visitors.

### Load third-party scripts only when needed

Sometimes you need to use external scripts. You could be using a chat service or a payment provider. One of the things you should do is to only load those scripts on pages where you actually use them.

On a chat it maybe for every page but for a payment provider it certainly wouldn't be the case. Don't include those script on every page.

When using a chat that you use on every page you could get a bit creative. For example you could have a little button that only loads the external script when you click it. For example:

```js
var button = document.querySelector('.chat-button')
button.addEventlistner('click', function() {
var script = document.createElement('script')
script.onload = function () {
  // Do something with the chat script if needed
}
script.src = 'https://chat.example.com/script.js'
document.head.appendChild(script)
}
```

To check if your site uses third-party scripts you can use the [Request Map Generator](https://requestmap.webperf.tools/) built by [Simon Hearne](https://twitter.com/simonhearne) _(thanks [Jan Klimo](https://twitter.com/janklimo/status/1203708198907047937))._

For [Simple Analytics](https://simpleanalytics.com) it looks like this:

![](https://i.imgur.com/L8PxoC1.jpg)

We use an external payment provider, but only load the script when you click on signup, hence in this image you don't see any external scripts.

## Do not give too much power to your CDN provider

If you use a CDN you are giving them data about your visitors and the power to load a different script then your visitors request.

To prevent your CDN provider tempering with the source of your scripts you can use [Subresource Integrity](https://developer.mozilla.org/en-US/docs/Web/Security/Subresource_Integrity) (SRI; the `integrity` attribute on your scripts). You need to create a hash of the source of the script and include this in the script tag via the `integrity` attribute. To generate the integrity hash you can use [srihash.org](https://www.srihash.org/).

```html
<script src="https://cdn.example.com/script.js" integrity="sha384-..."></script>
```

The `crossorigin` content attribute on media elements is a CORS settings attribute. This is needed to load scripts from other domains (a CDN domain for example). The `anonymous` keyword means that there will be no exchange of user credentials via cookies and some other data between your website and other domains. You specify it like this:

```html
<script
  src="https://cdn.example.com/script.js"
  integrity="sha384-..."
  crossorigin="anonymous"
></script>
```

To prevent giving the page your visitors are on you can add the `referrerpolicy` attribute with a `no-referrer` value to your script tags:

```html
<script
  src="https://cdn.example.com/script.js"
  integrity="sha384-..."
  referrerpolicy="no-referrer"
></script>
```

Although you are not sending the referrer here, browser do send the origin header with CORS requests. This means that your CDN provider still gets the domain where your visitors land on. If they record IPs they can track the browsing behaviour of your visitors. This can only be solved by choosing a CDN provider that anonymizes the IP addresses. The only CDN provider that currently offers IP anonomization is [BunnyCDN](https://bunnycdn.com/) _(we are not affiliated with BunnyCDN)_.

If you combine all above features the HTML will look similar to this:

```html
<script
  src="https://cdn.example.com/script.js"
  integrity="sha384-..."
  crossorigin="anonymous"
  referrerpolicy="no-referrer"
></script>
```

If you add scripts dynamically you can specify the above features as properties. The attributes are case sensitive. Both `crossOrigin` and `referrerPolicy` have one capital letter in them:

```html
const s = document.createElement("script"); s.src =
"https://cdn.example.com/script.js"; s.integrity = "sha384-..."; s.crossOrigin =
"anonymous" s.referrerPolicy = "no-referrer";
```

## Remove social widgets

Social media companies do not have a very good reputation for collecting data of your visitors. There are many plugins and ways to track users. Your visitors don't choose to be tracked by those companies, you do.

...Add https://en.wikipedia.org/wiki/UBlock_Origin

Your visitors can do something about it themselves by installing tracking blockers, but there will always people that don't know about this tracking or don't know how to prevent this from happening. That's why the EU came with the [GDPR](https://gdpr.eu/), California with the [CCPA](https://www.oag.ca.gov/privacy/ccpa), Brazil with [LGDP](http://www.planalto.gov.br/ccivil_03/_Ato2015-2018/2018/Lei/L13709.htm), and the UK with [PECR](https://ico.org.uk/for-organisations/guide-to-pecr/).

> On 29 July 2019, the Court of Justice of the European Union (the "CJEU") ruled that a company embedding on its website a social plugin, such as a Facebook “Like” button, can be considered a data controller, when the inclusion of the plugin results in the browser of a visitor fetching content from the plugin provider and sending personal data of the visitor to that provider. The CJEU found that although the company may not be found responsible for the subsequent processing of data carried out by the social plugin provider, it is nevertheless responsible for facilitating the collection and transmission of data to the plugin provider via the insertion of the plugin on the website – [fieldfisher.com](https://privacylawblog.fieldfisher.com/2019/cjeu-rules-that-companies-using-social-plugins-are-liable-for-the-collection-and-transmission-of-data)

Although you are not in control of what those platforms behind your widgets do with the data of your customers, you are still primarily/overall responsible.

Facebook for example does now allow custom share links:

[...]

On the internet you see the Twitter widget being used a lot. But is there really need to send the data of your visitors to Twitter when they just want to see a tweet?

[...]

## Don't trick your visitors

When browsing the internet you will find many example of websites trying to trick you in an opt-in for allowing to track you.

For example the home page of the New York Times. When you see a cross (X) you normally would close a dialog box without agreeing to what's being asked. The New York Times just sees it the same as "I agree":

![](https://i.imgur.com/MYUOIkf.jpg)

... ADD MORE EXAMPLES ...

### Marketing emails

If you have a business, there is great value by using the email address of your customers. Use it wisely to inform them about new features, help them getting around your tool, etc. It's a perk for your business. But if you're sending marketing emails to your customers, be sure they want it. You can ask during signup if it's okay for you to send them emails about your tool/service, or you ask if they are okay with you sending some setup guides or tips. Be aware that if you specify how you are going to use their email, and make sure you only use their email for that pupose.

#### How to keep a good reputation

Another thing with marketing emails is the unsubscribe header. Make sure you have the header setup as it improves your email reputation. The headers could look like this:

```
List-Unsubscribe: <https://example.com/unsub/?uuid=14b2-b2a1>, <mailto:unsubscribe@example.com>
```

In a lot of clients the unsubscribe link is placed close to the spam button. You want people to unsubscribe instead of hitting the spam button to prevent damaging your reputation.

## Where do you store your data

## Do not log or ask PII data when not needed

### Don't ask full names

Unless you really need it. Let people decide if they want to add their full name. Just ask for a first name if you want to address people in your marketing emails, but don't ask for a full name.

For people reading that are tired of coming up with fake names: there are [plenty of services out there](https://duckduckgo.com/?q=fake+name+generator) to help create a fake name.

### IP anonymization

This part is rather technical so bear with me. If you are a manager please forward this to your developers. IP anonymization is the most logical thing to do on your servers when talking about privacy. Yet, there are not that many examples on how to actually do it. A lot of processes on your servers log data. For example _NGINX_ logs data about every request (it's customizable) that comes in. This is great for debugging but it's less good for the data of your users. With _NGNIX_ you can't format the error logs so it will always error in the same format. This is very privacy unfriendly because it contains the full IP address of the user and usually the _User Agent_ (which can contain IDs when using the Facebook app).

> I could write a whole article about how Facebook (and other companies) uses their _User Agents_. Basically they fill them with a lot of extra data. To show an example, this is a _User Agent_ suffix of a Facebook app: `[FBAN/FBIOS;FBAV/221.0.0.0.0;FBBV/154514034;FBDV/iPhone9,4;FBMD/iPhone;FBSN/iOS;FBSV/12.3.0;FBSS/3;FBCR/Siminn;FBID/phone;FBLC/en_GB;FBOP/5;FBRV/155138002]`

### Filters in syslog

Simple Analytics uses _NGINX_ which in our case logs to _rsyslog_, often referred to as _syslog_. _rsyslog_ is ofter included in Linux distributions ([official website](https://www.rsyslog.com/)). Luckily _rsyslog_ comes with a great module that's called _mmanon_. This module can be used to filter IP addresses for both v4 and v6 from _rsyslog_ [version 7.3.7](https://www.rsyslog.com/doc/v8-stable/configuration/modules/mmanon.html). On your sever you can check which version of _rsyslog_ you have by running `rsyslogd -v`. In our server it shows version `8.32.0`.

You can enable IP anonymization with adding the following lines to your _rsyslog_ config file. The config file usually lives in `/etc/rsyslog.conf` or `/etc/rsyslog.d/50-default.conf`.

```bash
module(load="mmanon")
action(type="mmanon" mode="zero" ipv4.bits="32" ipv6.bits="128")
```

After you have changed this file make sure to restart _rsyslog_ with `service rsyslog restart`.

#### Next level syslog

If you want to go deeper you can setup some advanced filters to remove sensitive data within your log files or log services.

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

You can do way more, [in our config](https://gist.github.com/adriaanvanrossum/e692b0399f0ca8ab15005315ab0dd694) we hide IPs, credit cards and user agents.

### Use two-factor authentication

This one is more security related than privacy, but it's important either way.

If you want to secure the data of your users and prevent others accessing their data, use a two-factor authentication system. [Don't use SMS](https://duckduckgo.com/?q=sms+two-factor+authentication). Use [TOTP](https://en.wikipedia.org/wiki/Time-based_One-time_Password_algorithm) (Time-based One-time Password) which has lots of apps and integrations. It does not require internet connectivity and can be installed on multiple devices.

### Conclusion

While working on Simple Analytics, I'm constantly fighting the status quo by finding privacy friendly ways of handling visitor data. There is way too little information on how to actually prevent tracking in your own business.

I hope this article makes the web a bit more privacy friendly. [Please let me know](https://github.com/simpleanalytics/blog/issues/new) which tips I should add.
