---
title: 4 privacy-friendly Google Analytics alternatives
title_html: "4 privacy-friendly<br/>Google Analytics alternatives"
author_slug: iron
author: Iron Brands
excerpt: "How privacy-friendly are all the different Google Analytics alternatives really? Let's find out."
image: https://assets.simpleanalytics.com/blog/google-alternatives/spectrum-privacy-friendly-analytics.png
related_posts:
 - /blog/website-analytics-without-cookies
 - /blog/simple-analytics-for-marketers
 - /blog/italy-declares-google-analytics-illegal
 - /blog/why-its-time-to-move-away-from-google-analytics
lang: en
---

This write-up was long due. The call for Google Analytics alternatives hasn't been as loud as today. We believe it will become even louder in the future.

A changing business landscape in which data privacy plays a more prominent role has led organizations to rethink their digital practices.\
In the real world, we value our privacy, and so do we in the digital world.

Measures to ensure this are already in place with the adoption of privacy laws such as the [GDPR](https://gdpr-info.eu/), [PECR ](https://ico.org.uk/for-organisations/guide-to-pecr/what-are-pecr/)& CCPA. The most recent example of these laws in practice is the [Schrems II ruling](https://noyb.eu/en/austrian-dsb-eu-us-data-transfers-google-analytics-illegal) on the use of Google Analytics.

Consequently, the market for privacy-friendly alternatives is growing, but how privacy-friendly is everyone?

Let's find out!

{% include gif.html slug="spy-kids-better-look-closer" alt="Spy Kids: Better look closer" width="300" height="201" color="#594748" %}

This write-up focuses only on privacy. A breakdown based on web insights, ease of use, and costs is also in the pipeline, but for now, we will be looking at how privacy-friendly everyone really is...

The following criteria will form the basis for benchmarking the Google Analytics alternatives:

- Use of cookies
- Use of IP Addresses
- Data Transfers outside the EU
- Data ownership.

We will be looking at Google Analytics (as a base case), Simple Analytics, Plausible, Matomo, and Fathom.

Let's dive in

## Google Analytics

<img src="https://assets.simpleanalytics.com/blog/google-alternatives/google-analytics-dashboard.png" alt="Google Analytics dashboard of Fiks.nl" class="border" />
<p class="caption" markdown="1">
  The dashboard we all know
</p>

We are talking about alternatives, but it is good to use Google Analytics as a base case. They have received a lot of scrutiny over the past few months concerning privacy.

This is also why the call for privacy-friendly alternatives has never been this loud.

The current version of Google Analytics (universal analytics) uses cookies and also collects IP Addresses to track website visitors.

Google Analytics is free, but you pay with your data. The data they collect is not yours to keep. It's theirs. They transfer the data overseas and share it with third parties.

Google Analytics will change to a [new version](https://www.searchenginejournal.com/google-sunsetting-universal-analytics-in-2023/442168/) next year. The change is driven by a changing business landscape that demands less privacy-invasive ways of internet tracking. GA4 is therefore supposed to be more privacy-friendly (but it really isn't). You can check our analysis on GA4 [here](/google-to-sunset-universal-analytics-in-2023).

## Simple Analytics

<img src="https://assets.simpleanalytics.com/blog/google-alternatives/simpleanalytics-dashboard-top.png" alt="Simple Analytics dashboard" class="border" />
<p class="caption" markdown="1">
  The dashboard of Simple Analytics
</p>

Yeeey... we made our own Google Analytics alternatives list. We might be biased, but we try to benchmark ourselves on the above criteria as well as any other alternative.

Simple Analytics focuses on privacy. We did not just build Simple Analytics to comply with regulations. We genuinely think we can make the internet a little bit better while still providing in-depth insights to track your website performance.

We believe that the future of web analytics is cookieless; hence Simple Analytics is [cookieless by design](https://blog.simpleanalytics.com/website-analytics-without-cookies).

In addition, [we don't collect any personally identifiable information](https://docs.simpleanalytics.com/what-we-collect), not even in an anonymized way. Unique visitors are based on the referrer domain sent to us by the browser.

The [data is stored in The Netherlands](https://docs.simpleanalytics.com/locations), and the data is yours. The data will not be transferred overseas or shared with third parties.

## Plausible

<img src="https://assets.simpleanalytics.com/blog/google-alternatives/plausible-dashboard-top.png" alt="Plausible dashboard" class="border" />
<p class="caption" markdown="1">
  The dashboard of Plausible
</p>

At Simple Analytics, we respect Plausible. The owners, Marko & Uku, are dedicated builders. They are transparent about their revenue and processes and are highly motivated to make the internet a little bit safer, as do we.

Plausible is also cookieless by design. They store the data in Germany, and the data is yours. They don't transfer data overseas and don't share it with third parties.

The most significant difference between Simple Analytics is that Plausible collects IP addresses, albeit anonymized. This is better than just plainly collecting IP addresses, but we say it's still personal data. Hashes of IP addresses can be used as fingerprints to identify a person online, which is also personal data.

There has been a lot of debate about this as the GDPR isn't very explicit on different technologies used to identify a visitor (directly or indirectly). So let's briefly explain what IP hashes are and why we consider them as personal data.

## Are IP hashes personal data?

IP hashing is a cryptographic function that transforms an IP address (which simply is a numeric code) into an unrecognizable set of numbers. The hashed IP address can be used to obtain information about an individuals' behavior without directly storing the IP address.

IP hashing might be more privacy-friendly, but at Simple Analytics, we consider this as fingerprinting. Usually, fingerprinting is a technique to identify a specific user indirectly based on combining information such as timezone, pixel density, device identifier, and default language. You can do the same with a hash of an IP address.

[Article 4 of the GDPR](https://gdpr-info.eu/art-4-gdpr/) states that personal data relates to any information relating to an identified or identifiable natural person ('data subject'). It mentions various kinds of identifiers like cookies, device ID, and network IP addresses. It is written so that it doesn't describe specific technologies, like fingerprinting. At the least, it is still a murky area that we stay away from.

The main takeaway: an IP address is a fingerprint in itself. An IP hash can create a fingerprint when combined with other data points.

Plausible, Fathom, and others create an IP hash for 24 hours. With that information, it is able to provide a bit more insights. For example, unique visitor tracking is more accurate (for 24 hours) using IP addresses, and bounce rates can be measured with the collected sessions.

Even if it's only for 24 hours, we still think it's tracking. At Simple Analytics, we believe it's not needed to track visitors at all to provide valuable insights.

But how about the rest?

## Matomo

<img src="https://assets.simpleanalytics.com/blog/google-alternatives/matomo-dashboard.png" alt="Matomo dashboard" class="border" />
<p class="caption" markdown="1">
  The dashboard of Matomo
</p>

Matomo was the first Google Analytics challenger on the market. It is quite different from Simple Analytics and Plausible, and it looks more similar to Google Analytics. In terms of data collection, it also takes another stance. It is not cookieless by design.

In their default mode, Matomo still uses cookies to track website visitors, and therefore, you still need to use a cookie banner to ask for your visitors' consent. Matomo also collects IP addresses (in an anonymized way).

You do own the data yourself. The data is stored in the EU and not transferred overseas.

It is possible to use Matomo in a cookieless way as well.

We explain this in our [comparison between Matomo and Simple Analytics](https://blog.simpleanalytics.com/why-simple-analytics-is-a-great-alternative-to-matomo).

## Fathom

<img src="https://assets.simpleanalytics.com/blog/google-alternatives/fathom-dashboard-top.png" alt="Fathom dashboard" class="border" />
<p class="caption" markdown="1">
  The dashboard of Fathom
</p>

Fathom looks very similar to Plausible in their data collecting approach. Fathom also stores a hashed version of the IP address for 24 hours.

For privacy-friendly web analytics tools in general, it's always a balancing act between providing as many data insights as possible and protecting the privacy of internet users.

Whereas Simple Analytics leans towards privacy-first, Plausible and Fathom try to balance privacy-friendliness and data insights.

Fathom is not an EU company but stores its data in Germany. The data is yours, and it never leaves their EU servers (for European visitors).

## Conclusion

The market for web analytics tools is a crowded place. Capterra shows [us 361 software products in the web analytics category](https://www.capterra.com/web-analytics-software/?sortOrder=alphabetical). However, if you are looking for a privacy-friendly alternative, these are the ones worth looking at.

<table>
  <tr>
   <td></td>
   <td>Use of<br />cookies</td>
   <td>Use of IP addresses</td>
   <td>Data<br />Ownership</td>
   <td>Transfer of<br />Data overseas</td>
  </tr>
  <tr>
   <td>Google Analytics</td>
   <td>Yes</td>
   <td>Yes</td>
   <td>No</td>
   <td>Yes</td>
  </tr>
  <tr>
   <td>Simple Analytics</td>
   <td>No</td>
   <td>No</td>
   <td>Yes</td>
   <td>No</td>
  </tr>
  <tr>
   <td>Plausible</td>
   <td>No</td>
   <td>Yes (IP hash for 24 hours)</td>
   <td>Yes</td>
   <td>No</td>
  </tr>
  <tr>
   <td>Matomo</td>
   <td>Yes</td>
   <td>Yes (anonymized)</td>
   <td>Yes</td>
   <td>No</td>
  </tr>
  <tr>
   <td>Fathom</td>
   <td>No</td>
   <td>Yes (IP hash for 24 hours)</td>
   <td>Yes</td>
   <td>No</td>
  </tr>
</table>

Over the past few months, we've gotten a lot of questions about the differences between Simple Analytics and other privacy-friendly tools. I understand that you evaluate multiple alternatives (and you should) to determine what's best for your organization.

<img src="https://assets.simpleanalytics.com/blog/google-alternatives/spectrum-privacy-friendly-analytics.png" alt="Spectrum of privacy-friendly Google Analytics alternatives" class="border" />
<p class="caption" markdown="1">
  Spectrum of privacy-friendly Google Analytics alternatives
</p>

To articulate the differences in privacy-friendliness between the Google Alternatives, you can use the following one-liners to explain them to your colleagues.

Google Analytics: "They do use cookies, the data is not ours, and they do transfer the data overseas"

Simple Analytics: <mark>"They don't use any personal information, the data is ours, and they don't transfer the data overseas"</mark>

Plausible: "They don't use cookies, the data is ours, and they don't transfer the data overseas"

Matomo: "They use cookies, the data is ours, and they don't transfer the data overseas"

Fathom: "They don't use cookies, the data is ours, and they don't transfer the data overseas"

{% include gif.html slug="think-about-it-2" alt="Think about it" width="480" height="274" color="#73594d" %}

We are Adriaan & Iron, and we are trying to make the internet a little bit better. Are you with us? Feel free to [give us a try ](https://simpleanalytics.com/welcome)or check out our [live dashboard](https://simpleanalytics.com/simpleanalytics.com).
