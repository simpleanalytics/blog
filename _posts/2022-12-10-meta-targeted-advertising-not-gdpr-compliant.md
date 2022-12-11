---
title: "Meta targeted advertising not GDPR compliant"
author_slug: carlo
author: Carlo Cilento
excerpt: "The European Data Protection Board found that Meta has been illegally profiling users for targeted advertising on its platforms"
image: https://assets.simpleanalytics.com/blog/2022-meta-targeted-advertising/social-image-meta-targeted-advertising.png
image_no_text: https://assets.simpleanalytics.com/blog/2022-meta-targeted-advertising/social-image-meta-targeted-advertising.png
related_posts:
 - /blog/why-its-time-to-move-away-from-google-analytics
 - /blog/website-analytics-without-cookies
 - /blog/is-google-analytics-illegal-in-europe
 - blog/is-google-analytics-4-gdpr-compliant
---

As the [Wall Street Journal](https://www.wsj.com/articles/metas-targeted-ad-model-faces-restrictions-in-europe-11670335772) reported, the European Data Protection Board found that **Meta has been illegally profiling users for targeted advertising** on its platforms. The decision can be appealed but is unlikely to be overturned. No information about sanctions is available at the moment, but given the amount of personal data involved, we might see **a** **hefty fine**.

The decision stems from a complaint filed in 2018 by privacy NGO [noyb](https://noyb.eu/en/noyb-win-personalized-ads-facebook-instagram-and-whatsapp-declared-illegal) and overturns a previous ruling by the Irish data protection authority (DPC). While the decision has yet to be published, the picture is fairly straightforward since some information about the complaint has been publicly available for a long time.

In this blog, we will explain the deal with Meta and why it’s a **consequence of a broader problem with the business model behind social media**.

{% include gif.html slug="its-bigger-on-the-inside" alt="its-bigger-on-the-inside" width="500" height="500" color="#5a391b" %}

1.  The decision
2.  Data is not a commodity
3.  Conclusions

Let’s dive in!

## 1. The decision

To be clear, **the EDPB did** **not** **say that targeted advertising on social media platforms is in and of itself illegal**. The Board found that Meta was profiling users illegally because they were abusing a specific legal basis under the GDPR- the performance of a contract. This might seem like a minor detail, but it isn’t. Let’s unpack the issue.

As we explained [on our blog](https://www.simpleanalytics.com/blog/gdpr-101-legal-bases), under the GDPR, every data controller needs a **legal basis** to process data- a justification such as the data subject’s consent or a legal obligation. The GDPR includes a closed list of six legal bases, each with its own requirements.

Since the GDPR’s entry into force in 2018, Meta has been using **the performance of a contract** as a legal basis for serving users with personalized advertisements based on their online activity. By doing so, Meta was essentially claiming that personalized advertising is an essential part of their contract with the user (that is, the terms of service for Facebook and Instagram). Noyb claimed that Meta was abusing the legal ground of the contract and took legal action in 2018, filing the complaint that led to the EDPB’s decision.

The ruling itself is absolutely unsurprising. European case law has long clarified that the legal ground of contract only covers processing activities which are strictly necessary to the performance of the contract. This is obviously not the case with targeted advertising. Additionally, the EDPB itself clarified in its guidelines that contract is not a suitable legal basis for online behavioral advertising.

But why couldn’t Meta just rely on a different legal basis? It’s a bit complicated, so we’re going to keep things short and sweet here and include some more details in the notes. In a nutshell, **not relying on contract would have forced Meta to collect user consent instead**. This is a tricky proposition because a user could just refuse targeted advertising or opt out of it. As Internet users become more and more privacy-aware, this could **severely impact advertisement revenue** for the company.

Bottom line, Meta circumvented the rules and got away with it for four years.

## 2. Data is not a commodity

Meta is not the only big tech company struggling with the GDPR. For instance, [TikTok got in trouble with the Italian DPA](https://thehackernews.com/2022/07/tiktok-postpones-privacy-policy-update.html) because of legal bases not long ago. Google Analytics is also having its fair share of troubles and getting practically banned in several Member States, for different reasons (we wrote about this on our [blog](https://www.simpleanalytics.com/blog/the-complete-overview-from-101-noyb-complaints-to-banning-google-analytics)).

The core of the issue is that the GDPR (and the EU data protection framework in general) **treats privacy and data protection as fundamental rights**, whereas social networks (and many other tech companies) embody a surveillance-centered business model that **treats personal data as a commodity**.

These perspectives are **radically incompatible**. From a purely economic point of view, profiling is actually necessary to the performance of the contract because it’s a crucial part of Meta’s business model: if the company couldn’t profit from the contract, it would not be able to provide the service, nor would it have any incentive to do so. But under the GDPR, privacy and data protection are non-negotiable rights. The processing of personal data cannot be justified just because it’s part of a business model, no matter how widespread and successful.

Some critics of the GDPR claim that the Regulation is impracticable and out of touch with a data driven economy, but this is not the case. European institutions are well aware of the crucial role of data. This is why the GDPR strives to strike a balance between data protection rights and other fundamental rights, including the freedom to conduct a business.

But the GDPR also **draws a line between a data-driven economy and a surveillance economy**, and this line has been rightfully enforced against Meta.

## 3. Conclusions

The EDPB’s decision shows once again that the GDPR can be an effective tool to enforce privacy against surveillance-based business models. But enforcement is only a part of the picture. Consumers are increasingly aware of privacy issues and companies are starting to see the value of good, privacy-friendly data governance.

A move towards privacy-minded tools can play a big part in building a surveillance-free Internet. With [Simple Analytics,](https://www.simpleanalytics.com/) we are trying to facilitate this. We believe that you can get insights from your web analytics, without the need to collect personal information or install cookies in your visitors’ computer.

We believe in an independent web that is friendly to website visitors. If this resonates with you, feel free to [give us a try!](https://simpleanalytics.com/simpleanalytics.com)
