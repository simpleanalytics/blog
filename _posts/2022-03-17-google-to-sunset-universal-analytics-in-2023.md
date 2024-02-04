---
title: Google to sunset Universal Analytics in 2023
title_html: Google to sunset<br />Universal Analytics in 2023
author_slug: iron
author: Iron Brands
excerpt: "Google Analytics to sunset Universal Analytics in favor of GA4, but how privacy-friendly is GA4?"
image: https://assets.simpleanalytics.com/blog/socials/google-kill-universal-analytics.png
related_posts:
  - /blog/website-analytics-without-cookies
  - /blog/why-its-time-to-move-away-from-google-analytics
  - /blog/why-simple-analytics-is-a-great-alternative-to-google-analytics
  - /blog/simple-analytics-for-marketers
lang: en
last_modified_at: 2022-11-30
---

[Google just announced](https://blog.google/products/marketingplatform/analytics/prepare-for-future-with-google-analytics-4/) that it will sunset Universal Analytics in favor of G4 Analytics. This is a huge blow for marketers that have relied on the current version for a long time. Is this the right time to switch, or is G4 Analtyics worth it?

In short: Google will begin to sunset universal analytics on July 1, 2023. This means that from this date, Universal Analytics will stop processing new hits. Universal Analytics 360 properties will still be available until October 1, 2023. After that, you can only access your data in Universal Analytics for six months.

> Update: on October 27, Google announced it would push back the sunsetting of Universal Analytics 360 properties once again to July 2024. According to Russell Ketchum (Product Management Director for Google Analytics), the decision is meant to give larger organizations more time to switch to Google Analytics. As the press release notes, Google Analytics properties will still sunset in October 2023, so only paying users of Google 360 will benefit from the extension. Google also announced that they will be focusing most of their work on GA4 starting in 2023, which will result in a degradation of the UA experience.

> Earlier this year, the company also announced its Chrome browser will support third-party cookies until 2024- phasing them out one year later than originally planned. UA uses third-party cookies, so delaying its sunsetting has probably been on Google's mind for a while now.

## Why is Google to sunset Universal Analytics?

In the announcement, Google states that G4 Analytics is "the new standard" in today's challenging business environment.

They point out that G4 Analytics

<mark>...has the flexibility to measure different kinds of data</mark>\
<mark>...delivers a strong analytics experience that's designed for the future</mark>\
<mark>...allows businesses to see unified customer journeys across their website and apps</mark>

All of the above seem to be driven by a **changing ecosystem that calls for less privacy-invasive ways of collecting data**.

Thereby, Google acknowledges that the way they track website visitors across the internet is not sustainable in the long term.

But is "the new standard" really up to standard regarding privacy-friendliness?

{% include gif.html slug="really" alt="Really?" width="435" height="244" color="#7d6247" %}

## How privacy friendly is G4 Analytics really?

### IP Anonymization

The first privacy-focused change after the Universal Analytics sunset is that IP address is anonymized by default.

In the Universal Analytics version, the user IP was collected as a whole. However, it is possible to anonymize IP-address in Universal Analytics as well by adding a tag. In G4 Analytics, user IP is anonymized by default and cannot be changed back.

Well, this sounds like an improvement from a compliance perspective, but it is not really impactful. Anonymized IP addresses are still considered personal data according to the GDPR. [See our blog post on this topic](/blog/will-google-analytics-be-banned-in-the-eu).

### Server Location

[The scrutiny Google Analytics has undergone](/blog/will-google-analytics-be-banned-in-the-eu) in the wake of the ['Schrems ii'](https://iapp.org/news/a/the-schrems-ii-decision-eu-us-data-transfers-in-question/) ruling is still valid for G4 Analytics. Transferring data to US servers is still in conflict with [the GPDR](https://gdpr-info.eu/).

Also, with G4 Analytics, Google does not allow you to control where your data is stored.

### Use of Cookie banner

Regardless of tracking IP addresses, you need a cookie banner when installing non-functional cookies. Analytics cookies are non-functional cookies.

In their statement, Google pointed out that the measurement methodology is becoming obsolete (and I couldn't agree more). However, **Google Analytics will still rely on first-party cookies**.

Ditching third-party cookies is a good thing, but first-party cookies are still cookies and require consent. With GA4, you still need to use an annoying cookie banner on your website (and miss a lot of data).

### Limited Data Storage

This is the first meaningful improvement. With G4 Analytics, the time you can store data has decreased from (up to) 64 months to 2 or 14 months (based on your preferences).

The limited timeframe encourages you to only store data for the period you are using it.

### Deleting Individual User Data

In G4 Analytics, it's now possible to delete individual user data. In Universal Analytics, it was only possible to delete data within a set time range. This functionality is an improvement from a privacy perspective and makes it easier to respond to erasure requests under the GDPR.

What are meaningful privacy improvements?

| Feature                       |                                                                           |
| :---------------------------- | :------------------------------------------------------------------------ |
| IP Anonymization              | ![](https://assets.simpleanalytics.com/blog/github/svgs-cross-ga.svg)     |
| Server Location               | ![](https://assets.simpleanalytics.com/blog/github/svgs-cross-ga.svg)     |
| Use of Cookie Banner          | ![](https://assets.simpleanalytics.com/blog/github/svgs-cross-ga.svg)     |
| Deleting Individual User Data | ![](https://assets.simpleanalytics.com/blog/github/svgs-checkmark-ga.svg) |
| Limited Data Storage          | ![](https://assets.simpleanalytics.com/blog/github/svgs-checkmark-ga.svg) |

In conclusion, you could say that G4 Analytics is a bit more privacy-friendly than Universal Analytics. Still, in the end, it does not have any meaningful impact on GDPR compliance.

Therefore, It's a bit far-fetched to call G4 Analytics "the new standard" in a changing environment that calls for less privacy-invasive data-collecting measures.

{% include gif.html slug="nonono" alt="No no no!" width="480" height="336" color="#47695b" %}

## Is switching from Universal Analytics to G4 Analytics worth it?

There are a few angles from which you should answer this question. Taking privacy-friendliness into account is one thing, but is changing to G4 Analytics also worthwhile from a 'business' standpoint?

Whether you like it or not, the future of web analytics will be cookieless. Web Browsers like Firefox and Safari have already blocked third-party cookies, and even [Google Chrome announced](https://www.theverge.com/2021/6/24/22547339/google-chrome-cookiepocalypse-delayed-2023) that it will be phasing out with third-party cookies in 2023.

The world is heading in the right direction, and Google reluctantly moves with it, but it's doing everything to keep its business model alive.

Do you really want to invest your time and energy learning the ins and out of G4 Analytics while it won't futureproof your business? This might be the right time to switch to the good side.

## Losing your historical data

As said before, Google doesn't offer tools to migrate data between the two types of properties. At some point, you will lose this data when they sunset those properties.

[We built a Google Analytics importer](https://docs.simpleanalytics.com/import-google-analytics-data) to keep this historical data. At the same time, our customers don't start with an empty dashboard. Our importer can copy your data from Google Analytics 4 and Universal Analytics properties.

At Simple Analytics, we don't collect personal information. Therefore it doesn't matter much how long we keep the data. The data itself is not privacy invasive to its visitors it contains.

## Looking for an alternative after the Google Analytics sunset?

At [Simple Analytics](https://simpleanalytics.com/), we do things a bit differently. We are a two-person team that has built a privacy-first alternative to Google Analytics that uses no cookies or collects any personal data.

We have stripped the complexity from Google Analytics and designed [a one-page dashboard](https://simpleanalytics.com/simpleanalytics.com) that shows you everything you need to know.

{% include video.html width="1440" height="1044" slug="2022-03-17-dashboard" class="border" %}

We are cookieless by design and part of the future.

Don't take my word for it. Try[ for yourself](https://simpleanalytics.com/welcome).
