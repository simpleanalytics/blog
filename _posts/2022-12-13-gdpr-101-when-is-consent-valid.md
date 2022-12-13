---
title: "GDPR 101: When is consent valid?"
author_slug: carlo
author: Carlo Cilento
excerpt: "Short description of the post"
image: https://assets.simpleanalytics.com/blog/2022-gdpr-101-when-is-consent-valid/social-image-gdpr-101-when-is-consent-valid.png
image_no_text: https://assets.simpleanalytics.com/blog/2022-gdpr-101-when-is-consent-valid/social-image-gdpr-101-when-is-consent-valid.png
related_posts:
 - /blog/why-its-time-to-move-away-from-google-analytics
 - /blog/website-analytics-without-cookies
 - /blog/is-google-analytics-illegal-in-europe
 - blog/is-google-analytics-4-gdpr-compliant
draft: true
---


Consent is important in data protection because it allows individuals to control how their personal information is collected, used, and shared- nobody likes the idea that soameone else can monitor them or process their personal data without their consent! 

Consent is essential in the GDPR, which is why we wrote about it in our [blog](https://www.simpleanalytics.com/blog/gdpr-consent-101) a while ago. We also explained in our blog on legal bases that consent is not, in principle, required to process personal data under the GDPR: other legal bases exist in the GDPR[^1], each with its own use cases and limitations.

Consent is also **easy to abuse**: it’s not hard to force or trick someone into agreeing to something they don’t want. This is why data protection law (and law in general) sets out specific requirements for consent to be valid.

{% include gif.html slug="feel-violated" alt="feel-violated" width="480" height="270" color="#78605b" %}

The GDPR is no exception. Consent under the GDPR must be **freely given, specific, informed, and unambiguous[^2]**. Additionally, it must be possible to withdraw consent. These requirements are very important in practice!

1. [The requirements for consent](#1-the-requirements-for-consent)
2. [When is consent problematic? Some examples](#3-when-is-consent-problematic-some-examples)
4. [Conclusion](#4-conclusion)

Let’s dive in!

## 1. The requirements for consent

### 1.1 Freely given

In a nutshell, consent is freely given when **the data subject has a real choice in the matter[^3]**. This typically doesn’t happen when there is a **power imbalance** between the data controller and the data subject.

An **employment relationship** is a textbook example of constrained consent because an employer may take advantage of their position to pressure an employee to consent. As a general rule[^4], the employer cannot process employee data based on fake consent and needs to rely on a different legal ground instead.

Individual autonomy is an age-old problem in law: people may be free on paper while subject to economic, cultural and social pressure. Data protection law is no exception, so there is a grey area regarding freely given consent.

### 1.2 Specific

Consent is specific when it is **given for a specific purpose**. For example, you cannot ask for an email to provide your audience with a newsletter and then use the data to send promotions. In that case, you need to collect two distinct consents, one for each purpose.

This requirement goes hand in hand with the requirement for **informed consent** and with the principle of purpose limitation:

-   purpose limitation means that data must always be collected and processed with a specific, explicit, and legitimate purpose in mind
-   informed consent means the subject must know exactly what he is consenting to, including the purpose of the processing.

### 1.3 Informed

Consent is informed when the data subject is provided with certain information, including the controller's identity, the purpose of the processing, the types of data processed, the right to withdraw consent, and whether the data will be disclosed to third parties[^5].

Article 13 also plays a role here. The article is a laundry list of information that needs to be provided by the controller, whatever legal basis they might be relying on. Article 13 is the reason privacy policies are long and boring.

### 1.4 Unambiguous

Consent is unambiguous when given through a clear affirmative action. In other words, **there is no such thing as implicit consent under the GDPR**. This is why opt-out systems or pre-ticked boxes[^6] can never be used to collect valid consent.

The GDPR does not prescribe how consent should be collected as long as the collected consent is unambiguous. The data subject could sign a form, tick a checkbox or give oral consent. But as a rule of thumb, the controller should collect consent in a way that can be documented because providing proof of consent is its responsibility[^7].

The notion of unambiguous consent overlaps with that of explicit consent. Explicit consent can be considered a “reinforced” form of consent and functions as an exemption from specific rules about the processing of sensitive data, automated decision-making, and data transfers. So all consent must be unambiguous, but whether it is also explicit only matters in specific scenarios.

To put it mildly, the notion of explicit consent is not crystal clear. Implicit consent is never valid, so it’s hard to say what explicit means exactly and how explicit consent differs from unambiguous consent. But as a rule of thumb, it’s probably safe to think of explicit consent as very unambiguous consent.

## 2. When is consent problematic? Some examples

### 2.1 Bundled consent

“Bundled consent” is a sadly common situation where a customer is forced to consent to the processing of their data to conclude a contract, even though the contract doesn’t really require the processing. In other words, the data processing is “bundled” with the contract, typically as a form of payment.

To be clear, you can collect consent for processing data as part of a contract[^8], whether the processing is essential to the contract. The problem arises when you **blackmail a customer** by making this consent a deal-breaker.

Article 7 says that bundled consent is problematic concerning consent. Unfortunately, the Article doesn’t entirely outlaw the practice of bundled consent but rather gives a warning or “yellow card” of sorts. The wiggle room left by the Article allows companies some grey areas to take advantage of. As a result, some Internet services still use bundled consent to extract data as payment, especially when they enjoy a monopoly position and have little or no alternatives. On the other hand, DPAs and Courts can enforce Article 7 strictly- and we hope they do.

### 2.2 Cookie walls

“Cookie walls” are pop-ups implemented by websites (typically news outlets) to **prevent the user from accessing certain content unless they agree to the use of cookies.**

Visitors will often be given the option to refuse the processing in exchange for a paid subscription, leading to three alternatives: paying with money, paying with data, or not being able to access the content.

Cookie walls are similar to bundled consent in that they allow a controller to collect data as payment for content. This practice is understandable from an economic perspective: many users are unwilling to pay but willing to allow cookies, and publishers need advertising revenue to provide content. However, data is not a commodity under the GDPR, and a case can be made that consent collected by cookie walls is not freely given.

Additionally, the publisher can also generate revenue from non-personalized advertisements based on the content of the news- which doesn’t require the processing of personal data at all.

### 2.3 Deceptive design

“Deceptive design” or “dark patterns” is the practice of designing **unclear or deceiving UI to nudge a user towards a desired action,** such as purchasing a product, downloading software, subscribing to a service, or consenting to the processing of personal data.

Deceptive design is an especially serious problem with regards to cookie banners. Cookie banners often nudge users to accept cookies on their browser or device. Some make the “accept” option easily accessible while making the “refuse” option less visible on the screen- for example, by using a smaller font or a color that doesn’t stand out against the background. Other banners present the user with confusing choices such as “accept/manage preferences” or “accept/learn more”. The user can only refuse the processing by clicking the second option and manually turning off the option to process all non-essential cookies.

The average Internet visitor is presented with countless such banners while browsing. At some point, many users simply give up to click fatigue and accept all cookies. A case can be made that consent collected by deceptive cookie banners is not freely given. And consent aside, a case can also be made that the processing is neither fair nor transparent[^9].

Last year the European Data Protection Board set up a [cookie banner task force](https://edpb.europa.eu/news/news/2021/edpb-establishes-cookie-banner-taskforce_en), as a response to numerous complaints against deceptive cookie banners by NGO noyb. The last time such a task force was set up, Google Analytics ended up being banned in several EU Member States (we wrote about it [here](https://www.simpleanalytics.com/blog/the-complete-overview-from-101-noyb-complaints-to-banning-google-analytics)), so there is hope for a crackdown on deceptive banners in the future.

## 3. Conclusion

The requirements for consent are meant to ensure the user is in control of their data. Unfortunately, this is often not the case. Many companies want to collect as much data as possible, and often ignore data protection rules or find clever ways to circumvent them. Day by day, this hoarding, data-greedy mindset is turning the Internet into a surveillance machine.

But it doesn’t have to be like that. We at [Simple Analytics](https://www.simpleanalytics.com/) believe in a World Wide Web that is user-friendly and respectful of privacy. This is why we work to provide our customers with valuable analytics insights without collecting any personal data from the end user. This eases the customer’s compliance burden, streamlines data governance, and helps make the Internet a better place. If this resonates with you, feel free to [give us a try](https://simpleanalytics.com/welcome).

>[^1]: Art. 6 GDPR.
>[^2]: Art. 4 (11) GDPR.
>[^3]: EDPB Guidelines 05/2020 on consent under Regulation 2016/679, par. 13.
>[^4]: Exceptions are very narrow. See EDPB Guidelines 05/2020 on consent under Regulation 2016/679, par. 22.
>[^5]: WP29 Guidelines on consent under Regulation 2016/679, par. 3.3.1.
>[^6]: See [CJEU - C-673/17 - Planet49](https://gdprhub.eu/CJEU_-_C-673/17_-_Planet49).
>[^7]: Art. 5(2) and 24 GDPR.
>[^8]: To be clear: in this scenario consent is the legal basis for the processing, not contract. Consenting to the contract is not the same as consenting to the processing of the data. Also note that specific formal rules apply in this scenario: see Art. 7(2) GDPR.
>[^9]: Art. 5(1)(a) GDPR.
