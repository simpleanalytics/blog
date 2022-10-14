---
title: "Is Google Analytics 4 GDPR compliant?"
author_slug: iron
author: Iron Brands
excerpt: "Google Analytics is sunsetting universal analytics in favor of Google Analytics 4. But how compliant is GA4 really?"
image: https://assets.simpleanalytics.com/blog/2022-
image_no_text: https://assets.simpleanalytics.com/blog/2022-
related_posts:
 - /blog/why-its-time-to-move-away-from-google-analytics
 - /blog/why-simple-analytics-is-a-great-alternative-to-google-analytics
 - /blog/how-to-delete-google-analytics-in-4-steps
 - /blog/website-analytics-without-cookies
draft: true
---

First paragraph

{% include gif.html slug="spy-kids-better-look-closer" alt="Spy Kids: Better look closer" width="300" height="201" color="#594748" %}

<img src="https://assets.simpleanalytics.com/blog/google-alternatives/google-analytics-dashboard.png" alt="Caption of the image" class="border-radius" />
<p class="caption" markdown="1">
  Caption of the image
</p>

Rest of the article

Google Analytics has recently come under fire from European authorities for non-compliance with the GDPR rules on data transfers. Google promises that the latest version of its analytics tool will be more privacy-focused. They will [sunset Universal Analytics](https://blog.google/products/marketingplatform/analytics/prepare-for-future-with-google-analytics-4/) in favor of GA4 next year, and privacy has been the main driver of this change. But how "privacy-friendlier" will this version be?

Many companies look forward to Google Analytics 4 as a solution to the compliance puzzle. However, companies might be a little too optimistic. While there is no case law on GA4 yet, the existing case law suggests that **GA4 suffers from the same legal issues as UA**.

![](https://lh4.googleusercontent.com/mSmkqylGSqnAvbXD24dBI-r1txcEb27Gg5MmpmDkd95sjOOR1G29lVYgYndCD3JzO7iGdJ3BkQdO3cKHtN8IwA7vPrxn3H0XziRKMnMqZiD1jYrzBc_ljC0Ki1YJyFMTDufGW3_slkoOsS_PPVPhYtEKLm9t95pJKwQUFDKvIf_Y_OJ_e3hSoMQurQ)

1.  The core issues: Personal data and supplementary measures
2.  Google Analytics 4 transfers personal data
3.  Privacy is more than compliance

Let's dive in!

## 1. The core issues: personal data and supplementary measures

The legal issues with data transfers are complex and lengthy to explain. If you have time to kill, we have written about it extensively [here](https://www.simpleanalytics.com/blog/how-to-move-forward-with-data-transfers-between-the-eu-us).

In a nutshell, the [Schrems II ruling](https://iapp.org/news/a/the-schrems-ii-decision-eu-us-data-transfers-in-question/) of the EU Court of Justice invalidated a data transfer framework that allowed for easy data transfers to the US. European companies now need to rely on a mechanism called standard contractual clauses to transfer data overseas. In addition, they need to implement supplementary measures on top of these clauses to protect data from State surveillance.

Right after the Schrems II ruling, privacy NGO noyb filed **101 complaints** before several European DPAs against websites using Google Analytics and Facebook Connect. The European Data Protection Board (the organization gathering all European DPAs) later formed a **task force** to coordinate the approach at a European level.

So far, this coordinated approach has led the [Austrian](https://gdprhub.eu/index.php?title=DSB_(Austria)_-_2021-0.586.257_(D155.027)), [French](https://gdprhub.eu/index.php?title=CNIL_(France)_-_Google_Analytics_(no_case_number)), and [Italian](https://gdprhub.eu/index.php?title=Garante_per_la_protezione_dei_dati_personali_(Italy)_-_9782890) DPAs to **declare Google Analytics unlawful**. Additionally, in a recent press release, the Danish authority essentially said the same, and the Dutch DPA announced earlier this year that it might[ follow suit](https://www.techzine.eu/news/privacy-compliance/71153/google-analytics-may-be-banned-in-the-netherlands/).

The core of the complaints is the supplementary measures required by the Schrems II ruling. No effective measures currently exist for GA and any other cloud-based services that need to process data in the clear. It follows that Google can only comply with the GDPR by not processing any personal data in the U.S. at all, and this is not the case. Also, not for Google Analytics 4.

## 2. Google Analytics 4 transfers personal data

Google advertised GA4 as a move toward a cookieless and privacy-friendly web analytics model, but their new analytics tool is not entirely cookieless. GA4 ditched third-party cookies but [employs a single first-party cookie called Client ID](https://support.google.com/analytics/answer/11593727?hl=en). All cookies, including first-party cookies, are **personal data** under the GDPR.

GA4 also uses an identifier called **User-ID**. User IDs are not cookies, but a different tool GA uses to track users across devices. They are **personal data** because they allow individual users to be singled out among website traffic. The same goes for the **unique ID** , a different parameter processed by Google Analytics to generate a User ID.

**Data linkage** is another crucial factor. GA4 processes many events and metrics that are not sensible data in and of itself but may be combined to single out a user. Crucially, Google also collects personal data from users who are logged into their **Google account**. This data can be linked with other data gathered by GA4 to easily make a user identifiable, as noted by European authorities in recent decisions.

Transferring personal data to the US is the problem at hand. Google Analytics 4 does not fix this. A Google Analytics 4 setup still transfers personal data to the US.

## 3. Privacy is more than compliance

So far, we have taken a look at GA4's compliance with the GDPR. But what about its general privacy implications?

Let's start with the good notes. GA4 is definitely more privacy-friendly in the way it handles IP addresses since they are neither logged nor stored. For comparison, UA always stores IP addresses and only offers an optional IP anonymization protocol (which European DPAs held to be ineffective). Ditching third-party cookies is also a step in the right direction.

On the other hand, the User-ID system **encourages very invasive tracking practices**. It is essentially a two-step system where the website itself collects certain data to identify a user cross-platform. Based on this data, the website generates a unique ID and provides it to Google. Google then generates a User ID for each unique ID provider and tracks the parameter across devices.

![](https://lh4.googleusercontent.com/URdPb9HaKqIBskP2bMSNiZjRu_O591cuh7XBCHSRQkWui_koiAkwaqFnl65lcYAocZEddaJPNBW8PnXQq08ahyGT1Hta9q8eta1SYXcBFqk7LP8-evAdRSKBlm5WU_L_LcDN38jzaAn04llVNIuaQHMSVymAH8mq6UgH5Y_isIt5GQgcFCIzfoEQuA)

As soon as GA4 becomes the standard, websites will have an incentive to track users and will predictably look for any excuse to collect the data they need for identifying users across devices. They may start locking content behind a registration in order to collect credentials and generate a unique ID, in a similar fashion to how "cookie walls" essentially require data as payment for a "walled" article.

Compliance-wise, this can easily go wrong. We expect to see websites collecting login credentials with the user's consent without informing a user that the credentials will be used in order to track their behavior for analytics purposes, which is a violation of the GDPR. Or they may inform the user but also force them to consent to being tracked in order to register - which is an instance of "bundled" consent. Crucially, generating a unique ID is entirely the customer's responsibility under GA's Terms of Service, and Google will not be responsible for any violation.

Alternatively, websites might look for other "creative" ways to track their users. For example, they may employ probabilistic tracking - that is, gathering a bunch of data such as IP, device location, and browsing data and running it through algorithms to estimate the probability that two devices belong to the same user. It sounds invasive, and it is.

Bottom line: Google is **creating a potential privacy nightmare and avoiding responsibility** by outsourcing some of the tracking work to the customers themselves.

## Final Thougths

There is no case law on GA4's data transfers yet. We at [Simple Analytics](https://www.simpleanalytics.com/) don't have a crystal ball, but based on existing case law and Google's own documentation, **the use of Google Analytics 4 is not GDPR compliant**.

Not only does Google Analytics 4 operate within the law, but we also believe it's a very privacy-invasive model of analytics that encourages websites to track their users.

At Simple Analytics, we believe that you don't need to track website visitors or collect personal data. We provide the [insights you need](https://simpleanalytics.com/simpleanalytics.com) without invading the privacy of your visitors and being 100% GDPR compliant.

We believe in creating an independent web that is friendly to website visitors. If this resonates with you, feel free to [give us a try](https://simpleanalytics.com/welcome).
