---
title: Will Google Analytics be banned in the EU?
author_slug: iron
author: Iron Brands
excerpt: "On the 13th of January, the Dutch Data Protection Authority (AP) openly questioned the legal use of Google Analytics in The Netherlands. In its statement, the AP implied that the use of Google Analytics may be banned in the future. In this article we explain this in detail."
image: https://assets.simpleanalytics.com/images/blog/why-simple-analytics-is-a-great-alternative-to-google-analytics/ga-vs-sa.png
lang: en
nl: /wordt-google-analytics-straks-verboden-in-de-eu
---

On the 13th of January, the Dutch Data Protection Authority (AP) [openly questioned the legal use of Google Analytics](https://autoriteitpersoonsgegevens.nl/nl/onderwerpen/internet-telefoon-tv-en-post/cookies#hoe-kan-ik-bij-google-analytics-de-privacy-van-mijn-websitebezoekers-beschermen-4898) in The Netherlands. In its statement, the AP implied that the use of Google Analytics may be banned in the future.

This comes after the DSB (the Austrian equivalent of AP) [confirmed the use of Google Analytics to be in violation of GDPR regulation.](https://noyb.eu/en/austrian-dsb-eu-us-data-transfers-google-analytics-illegal)

We've dug a bit deeper to see what's really going on right now.

Let's explore!

{% include gif.html slug="going-on-a-adventure" alt="Going on a adventure" width="400px" %}

1.  [The Complaint](#1-the-complaint)
2.  [The Ruling](#2-the-ruling)
3.  [Google's response](#3-googles-response)
4.  [The implications](#4-the-implications)

## 1. The Complaint

On the 14th of August 2020, someone (let's call it the 'data subject') visited a website on health topics, while logged in with his/her personal credentials. The website in question used [Google Analytics](https://analytics.google.com/analytics/web/) to track and monitor their website visitors.

A few days laters, On the 18th of August 2020, [NOYB](https://noyb.eu/en) (an NGO for digital rights) filed a complaint with the DSB on behalf of the 'data subject'. The complaint was filed against both the website provider and Google, as the owner of Google Analytics.

The complaint argued that transferring data to Google violates GDPR regulation, as Google qualifies as an "electronic communication service provider". This means that Google can be ordered to disclose data to US intelligence services on EU citizens. This means, that personal data of EU citizens is insuffieciently protected from US surveillance and therefore is in violation of GDPR regulation.

This is the critical point in the complaint. To put it bluntly: It's not about the use of Google Analytics, it's about the transfer of your personal data to US providers.

## 2. The Ruling

It's the first complaint resulting into a decision in relation to the so-called ["Schrems II"](https://iapp.org/news/a/the-schrems-ii-decision-eu-us-data-transfers-in-question/), which refers to the ruling that transferring data to US providers violates GDPR regulation. This has been the ruling since July 2020, but has lagely been ignored by data processors until now.

The complaint filed by NOYB, on behalf of the data subject, included multiple submissions from both sides over the course of 1,5 years. Google argued that even if there had been a transfer, the data would not qualify as personal data because it could not be assigned to the 'data subject'. In addition, they argued that a "risk-based approach" should be taken into account, as the risk of actually having to disclose the data was very low.

The [DSB](https://www.data-protection-authority.gv.at/) ruled differently and waived most of the arguments raised by Google.

Google qualifies as an "electronic communication service provider" and can be ordered to disclose personal data. The level of protection of personal data is therefore considered to be inadequate. Additional measurements, put in place by Google, were considered to be insufficient. They could by no means prevent the disclosure of personal data to the US intelligence services.

## 3. Google's Response

Russell Ketchum, Head of Product Management of Google Analytics, [responded on behalf of Google](https://blog.google/around-the-globe/google-europe/google-analytics-facts/). He stated that "Google Analytics helps consumers with compliance by providing them with a range of controls and resources". He said that IP addresses can be anonymized and that data collection can be disabled and deleted (on request).

I think he completely misses the point here. In his response, he mainly talks from the website owner's point of view. He states that organizations control the data they collect. However, its not about website owners, it's about website visitors. Their data should be protected and that's what the GDPR is for.

The point is the tranfer of data to US providers, which are subject to surveillance by the US government, like Google. He only addresses one sentence to this, stating that before any data is transferred to servers in the US, IP adresses are anonymized.

This still is in violation of [GDPR regulation](https://lawspeed.com/gdpr-transfers-of-data-to-the-united-states/). The DSB ruled that even anonymized IP addresses are personal data given the potential for it to be combined with other digital data, to identify a visitor. This is also were most privacy-friendly alternatives to Google Analytics, go wrong. At Simple Analytics, we never ever [collect your IP address](https://docs.simpleanalytics.com/what-we-collect), not even in an anonymized way, in contrast to other privacy-friendly alternatives.

## 4. The implications

Bottom line: This is a sound decision, but not a new one. It's a confirmation on what has been ruled in July 2020, but now it seems to have more impact. Personally, I have the feeling that the law will now be enforced.

If we believe this is the case, I would expect more EU member states to follow the Austrian example. The NOYB has filed a total of 101 complaints in more EU member states and speaks of a "coordinated response". The Netherlands is the first one to openly question the legal use of Google Analytics after Austria.

There are two solutions as Max Schrems (Honourary member of NOYB) noted. Either US providers will have to host foreign data outside the US or the US complies with proper data protection regulation.

If we fail to implement one of the above mentioned solution, we will be using different products accross the pond going forward. Either way, this provides the opportunity for others to compete with Google and 'Big Tech' as a whole.

We at [Simple Analytics](https://simpleanalytics.com/) have built a privacy-first alternative to Google Analytics. Our mission is to show organizations web analytics can be done differently by providing accurate insights whilst being GDPR compliant out-of-the-box. In addition, you never have to worry if your visitor's data is transferred to US providers, as [our servers are located](https://docs.simpleanalytics.com/locations) in The Netherlands. [Give us a try](https://simpleanalytics.com/welcome).

Cheers,

Adriaan & Iron

<img
  loading="lazy"
  class="avatar"
  src="https://assets.simpleanalytics.com/images/people/adriaan.jpg"
  referrerpolicy="no-referrer"
  alt="Adriaan van Rossum"
/><img
  loading="lazy"
  class="avatar"
  src="https://assets.simpleanalytics.com/images/people/iron.jpg"
  referrerpolicy="no-referrer"
  alt="Iron Brands"
/>
