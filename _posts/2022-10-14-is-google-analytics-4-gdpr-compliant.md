---
title: "Is Google Analytics 4 GDPR compliant?"
author_slug: carlo
author: Carlo Cilento
excerpt: "Google Analytics is sunsetting universal analytics in favor of Google Analytics 4. But how compliant is GA4 really?"
image: https://assets.simpleanalytics.com/blog/2022-is-google-analytics-illegal-in-europe/compliant-social-image.png
image_no_text: https://assets.simpleanalytics.com/blog/2022-is-google-analytics-illegal-in-europe/compliant-social-image-no-text.png
related_posts:
 - /blog/why-its-time-to-move-away-from-google-analytics
 - /blog/why-simple-analytics-is-a-great-alternative-to-google-analytics
 - /blog/how-to-delete-google-analytics-in-4-steps
 - /blog/website-analytics-without-cookies
last_modified_at: 2022-11-08
---

Google Analytics has recently come under fire from European authorities for non-compliance with the GDPR rules on data transfers. Google promises that the latest version of its analytics tool will be more privacy-focused. They will [sunset Universal Analytics](https://blog.google/products/marketingplatform/analytics/prepare-for-future-with-google-analytics-4/) in favor of GA4 next year, and privacy has been the main driver of this change. But how "privacy-friendlier" will this version be?

Many companies look forward to Google Analytics 4 as a solution to the compliance puzzle. However, companies might be a little too optimistic. While there is no case law on GA4 yet, the existing case law suggests that **GA4 suffers from the same legal issues as UA**.

{% include gif.html slug="are-you-sure" alt="are you sure" width="480" height="400" color="#584b4b" %}

1.  [The core issues: Personal data and supplementary measures](#1-the-core-issues-personal-data-and-supplementary-measures)
2.  [Google Analytics 4 transfers personal data](#2-google-analytics-4-transfers-personal-data)
3.  [Privacy is more than compliance](#3-privacy-is-more-than-compliance)

Let's dive in!

## 1. The core issues: personal data and supplementary measures

The legal issues with data transfers are complex and lengthy to explain. If you have time to kill, we have written about it extensively [here](https://www.simpleanalytics.com/blog/how-to-move-forward-with-data-transfers-between-the-eu-us).

In a nutshell, the [Schrems II ruling](https://iapp.org/news/a/the-schrems-ii-decision-eu-us-data-transfers-in-question/) of the EU Court of Justice invalidated a data transfer framework that allowed for easy data transfers to the US. European companies now need to rely on a mechanism called standard contractual clauses to transfer data overseas. In addition, they need to implement supplementary measures on top of these clauses to protect data from State surveillance.

Right after the Schrems II ruling, privacy NGO noyb filed **101 complaints** before several European DPAs against websites using Google Analytics and Facebook Connect. The European Data Protection Board (the organization gathering all European DPAs) later formed a **task force** to coordinate the approach at a European level.

So far, this coordinated approach has led the [Austrian](https://gdprhub.eu/index.php?title=DSB_(Austria)_-_2021-0.586.257_(D155.027)), [French](https://gdprhub.eu/index.php?title=CNIL_(France)_-_Google_Analytics_(no_case_number)), and [Italian](https://gdprhub.eu/index.php?title=Garante_per_la_protezione_dei_dati_personali_(Italy)_-_9782890) DPAs to **declare Google Analytics unlawful**. Additionally, in a recent press release, the Danish authority essentially said the same, and the Dutch DPA announced earlier this year that it might[ follow suit](https://www.techzine.eu/news/privacy-compliance/71153/google-analytics-may-be-banned-in-the-netherlands/).

The core of the complaints is the supplementary measures required by the Schrems II ruling. No effective measures currently exist for GA and any other cloud-based services that need to process data in the clear[^1]. It follows that Google can only comply with the GDPR by not processing any personal data in the U.S. at all, and this is not the case. Also, not for Google Analytics 4.

<img src="https://assets.simpleanalytics.com/blog/2022-is-google-analytics-illegal-in-europe/compliant-social-image-no-text.png" alt="Is GA4 GDPR compliant" class="border-radius" />
<p class="caption" markdown="1">
</p>

## 2. Google Analytics 4 transfers personal data

Google advertised GA4 as a move toward a cookieless and privacy-friendly web analytics model, but their new analytics tool is not entirely cookieless. GA4 ditched third-party cookies but [employs a single first-party cookie called Client ID](https://support.google.com/analytics/answer/11593727?hl=en). All cookies, including first-party cookies, are **personal data** under the GDPR[^2].

GA4 also uses an identifier called **User-ID**. User IDs are not cookies, but a different tool GA uses to track users across devices. They are **personal data** because they allow individual users to be singled out[^3] among website traffic. The same goes for the **unique ID**[^4], a different parameter processed by Google Analytics to generate a User ID.

**Data linkage** is another crucial factor. GA4 processes many events and metrics that are not sensible data in and of itself but may be combined to single out a user. Crucially, Google also collects personal data from users who are logged into their **Google account**. This data can be linked with other data gathered by GA4 to easily make a user identifiable, as noted by European authorities in recent decisions.

Transferring personal data to the US is the problem at hand. Google Analytics 4 does not fix this. A Google Analytics 4 setup still transfers personal data to the US.

## 3. Privacy is more than compliance

So far, we have taken a look at GA4's compliance with the GDPR. But what about its general privacy implications?

Let's start with the good notes. GA4 is definitely more privacy-friendly in the way it handles IP addresses since they are neither logged nor stored. For comparison, UA always stores IP addresses and only offers an optional IP anonymization protocol (which European DPAs held to be ineffective). Ditching third-party cookies is also a step in the right direction.

On the other hand, the User-ID system **encourages very invasive tracking practices**. It is essentially a two-step system where the website itself collects certain data to identify a user cross-platform. Based on this data, the website generates a unique ID and provides it to Google. Google then generates a User ID for each unique ID provider and tracks the parameter across devices.

<img src="https://assets.simpleanalytics.com/blog/2022-is-google-analytics-4-gdpr-compliant/visitor-tracking.png" alt="website visitor tracking" class="border-radius" />
<p class="caption" markdown="1">
</p>

As soon as GA4 becomes the standard, websites will have an incentive to track users and will predictably look for any excuse to collect the data they need for identifying users across devices. They may start locking content behind a registration in order to collect credentials and generate a unique ID, in a similar fashion to how "cookie walls" essentially require data as payment for a "walled" article.

Compliance-wise, this can easily go wrong. We expect to see websites collecting login credentials with the user's consent without informing a user that the credentials will be used in order to track their behavior for analytics purposes, which is a violation of the GDPR[^5]. Or they may inform the user but also force them to consent to being tracked in order to register - which is an instance of "bundled" consent[^6]. Crucially, generating a unique ID is entirely the customer's responsibility under GA's Terms of Service, and Google will not be responsible for any violation.

Alternatively, websites might look for other "creative" ways to track their users. For example, they may employ probabilistic tracking - that is, gathering a bunch of data such as IP, device location, and browsing data and running it through algorithms to estimate the probability that two devices belong to the same user. It sounds invasive, and it is.

Bottom line: Google is **creating a potential privacy nightmare and avoiding responsibility** by outsourcing some of the tracking work to the customers themselves.

## Final Thougths

There is no case law on GA4's data transfers yet. We at [Simple Analytics](https://www.simpleanalytics.com/) don't have a crystal ball, but based on existing case law and Google's own documentation, **the use of Google Analytics 4 is not GDPR compliant**.

Not only does Google Analytics 4 not operate within the law, but we also believe it's a very privacy-invasive model of analytics that encourages websites to track their users.

At Simple Analytics, we believe that you don't need to track website visitors or collect personal data. We provide the [insights you need](https://simpleanalytics.com/simpleanalytics.com) without invading the privacy of your visitors and being 100% GDPR compliant.

We believe in creating an independent web that is friendly to website visitors. If this resonates with you, feel free to [give us a try](https://simpleanalytics.com/welcome).

> [^1]: Recommendations 01/2020 on measures that supplement transfer tools to ensure compliance with the EU level of protection of personal data, par. 94.
> [^2]: EDPB Opinion 5/2019 on the interplay between the ePrivacy Directive and the GDPR, in particular regarding the competence, tasks and powers of data protection authorities, par. 29.
> [^3]: Recital 26 GDPR.
> [^4]: Using personally identifiable information (PII) as a unique ID is against GA Terms of Service. But the notion of personal data under the GDPR is wider than that of PII as understood by Google. This is pointed out by [Google themselves](https://support.google.com/analytics/answer/7686480?hl=en#:~:text=Google%20interprets%20PII%20as%20information,mailing%20addresses.).
> [^5]: Art. 13(1) GDPR. If consent is collected, the requirements that consent be informed and specific under Art. 4(11) is also violated.
> [^6]: Art. 7(4) GDPR doesn’t forbid bundled consent outright but describes it as problematic.
