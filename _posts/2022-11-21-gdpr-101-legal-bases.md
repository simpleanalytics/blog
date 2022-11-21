---
title: "GDPR 101: legal bases"
author_slug: carlo
author: Carlo Cilento
excerpt: "This article takes a closer look at the different legal bases you can use for processing data under the GDPR"
image: https://assets.simpleanalytics.com/blog/2022-
image_no_text: https://assets.simpleanalytics.com/blog/2022-
related_posts:
 - /blog/why-its-time-to-move-away-from-google-analytics
 - /blog/is-google-analytics-illegal-in-europe
 - /blog/website-analytics-without-cookies
 - /blog/is-google-analytics-4-gdpr-compliant
draft: true
---

This article is a follow-up to our older blog about [consent under the GDPR](https://www.simpleanalytics.com/blog/gdpr-consent-101), where we briefly explained how consent works and what the limitations of consent are. We briefly mentioned that consent is not always necessary and that personal data can sometimes be lawfully processed without a data subject's consent.

Today we will look closely at all the other **legal bases** for processing data under the GDPR. That's enough material to write a book about, so we will keep it as short and straightforward as possible.

{% include gif.html slug="i-bet-you-do" alt="i-bet-you-do" width="480" height="270" color="#2f2c2f" %}

1.  [What is a legal basis?](#1-what-is-a-legal-basis)
2.  [What are the legal bases under the GDPR?](#2-what-are-the-legal-bases-under-the-gdpr)
3.  [What legal basis should I choose?](#3-what-legal-basis-should-i-choose)
4.  [The legal bases](#4-the-legal-bases)
    1.  [Contract](#41-contract)
    2.  [Legitimate interest](#42-legitimate-interest)
    3.  [Legal obligation](#43-legal-obligation)
    4.  [Vital interest](#44-vital-interest)
    5.  [Public interest or exercise of a public authority](#45-public-interest-or-exercise-of-a-public-authority)

Let's dive in!

## 1. What is a legal basis?

In a nutshell: **to process data lawfully[^1], you need to rely on one of six legal bases listed by Article 6 GDPR**. From a practical standpoint, consider these conditions as **alternative requirements** that must be satisfied when data needs to be processed.

## 2. What are the legal bases under the GDPR?

Art. 6(1) lists **six legal bases**:

-   consent
-   the performance of a contract
-   compliance with a legal obligation
-   the vital interest of the data subject or another natural person
-   performance of a task in the public interest/exercise of a public authority
-   the legitimate interest of the controller

These legal bases come with **specific requirements**, which can be considered a set of "pros and cons." For example, consent needs to be *freely given, specific, informed, and unambiguous"[^2]*. If these requirements cannot be met, another ground must be used. Sometimes two or more grounds are available, while at other times, no ground may be available at all, in which case the data cannot be processed.

It should be noted that there is **no order of priority** between legal grounds. For instance, a data controller is free to choose between consent (listed first) and legitimate interest (listed last), provided that the requirements for each ground can be met in that specific scenario.

## 3. What legal basis should I choose?

As we said, each ground comes with specific requirements. Sometimes only one will be available, so you have no choice. At other times you might have the luxury of choosing between two or more.

Each legal basis has pros and cons. For example, let's assume you can choose between consent and legitimate interest. If you choose consent, then you need to collect in the first place. You also must ensure that the consent requirements (freely given, informed, specific, unambiguous) are satisfied. Finally, you should be aware that consent can be withdrawn and be prepared to deal with that possibility.

If you rely on legitimate interest instead, you don't need to collect consent, and you don't need to worry that consent might be withdrawn later. But you will need to balance your interest with the data subject's rights, and the subject may object to the processing (more on this later).

So it comes down to a **case-by-case assessment**. For example, if the processing is very invasive, then your legitimate interest may be hard to balance, and consent may be a better choice. On the other hand, if you are very concerned about the withdrawal of consent, you may want to consider legitimate interest instead. There really is no one-size-fits-all solution, which makes it fun.

That being said, all grounds have specific requirements, and as a result, some are more readily available to certain controllers. Companies and other private entities typically rely on consent, contract, and legitimate interest. On the other hand, public entities usually rely on either legal obligation or public interest/authority[^3].

<img src="https://assets.simpleanalytics.com/blog/google-alternatives/google-analytics-dashboard.png" alt="Caption of the image" class="border-radius" />
<p class="caption" markdown="1">
  Caption of the image
</p>

## 4. The legal bases

We already discussed consent, so we'll look at the other grounds. There is much to say about legal grounds, and we can only scratch the surface here.

### 4.1 Contract

Under Art. 6(1)(b) GDPR, you can process data when the processing is *"necessary for the performance of a contract"* with the data subject or to enter a contract at their request. For example, if you are shipping goods to a customer, you need a delivery address and contact information to ensure the shipping goes well. You can process this data based on the performance of your contract with the customer.

Contract is a convenient and hassle-free legal basis. On the other hand, it is pretty restrictive as to what data can be processed because the notion of necessity must be **interpreted strictly** and in reference to the actual object of the contract.

In other words, you cannot provide for the processing of unnecessary data in a contract as a convenient excuse to rely on this legal ground. DPAs won't let you cheat the system like that. That being said, it is not always clear whether the processing of certain data is essential to a contract, so there can be some gray areas in practice.

There needs to be some clarification between the grounds of contract and consent. To be clear: consenting to the contract and consenting to the processing of the data is not the same. Still, when the processing is part of a contract, it's a good idea to explicitly identify the legal basis for the processing of the data, just to be safe. This can avoid some headaches down the road and helps the data controller comply with its transparency duties under Art. 13

### 4.2 Legitimate interest

Under Art. 6(1)(f), data can be processed when necessary for pursuing a **legitimate interest** of the controller or a third party. For instance, a company can install surveillance cameras on its premises based on its legitimate interest in protecting its property.

The notion of legitimate interest is very wide. It can cover a person's interest in protecting their property, a company's interest in running their business or advertising a product, an NGO's interest in pursuing humanitarian goals, and the interest of a website to generate ad revenue. Even a general interest can sometimes be invoked to rely on legitimate interest.

As a result, *legitimate interest* is a very flexible ground and can be used for many purposes. But this flexibility comes with a specific limitation (and compliance burden): the controller must ensure that their interest is not *overridden* by the interests, rights, and freedoms of the data subjects.

This assessment is commonly referred to as **balancing**. In a nutshell, balancing consists of three questions[^4]: is the interest legitimate? Is the processing necessary? And does the processing disproportionately impact the position of the data subject?

This sounds simple enough, but it is quite tricky. Balancing is a **case-by-base assessment** and needs to take many variables into account. Returning to our example: are the cameras active all the time or only outside working hours? Are the cameras placed in the company parking lot, or are they inside the workplace where they can capture footage of employees as they work? Do the cameras record footage of pedestrians moving down the street? All of these questions are relevant to the balancing of legitimate interest.

In practical terms, the controller will typically carry out the balancing test by drafting an assessment *(legitimate interest assessment or LIA)*. While not mandatory under the GDPR, a written assessment is the easiest way for the controller to show that they did their homework regarding the balancing[^5].

There is *much* more to say about balancing[^6], and we can't go too deep here. But the bottom line is that balancing is tricky, and you should consider this when deciding to rely on legitimate interest. On the other hand, legitimate interest is a very flexible ground, so it may be your only choice in some scenarios.

Two last points. First, the GDPR provides that public authorities cannot invoke this ground in performing their tasks[^7]. Second, the data subject has a **right to object** to the processing of their data based on legitimate interest[^8]. Notably, this right functions as an **opt-out mechanism** from the processing of personal data for direct marketing[^9]. We won't go into more detail, but if you're curious, [the ICO's website is a good source of information on this topic](https://ico.org.uk/for-organisations/guide-to-data-protection/guide-to-the-general-data-protection-regulation-gdpr/individual-rights/right-to-object/#:~:text=Individuals%20have%20the%20absolute%20right,authority%20vested%20in%20you%3B%20or) (there is no difference between the GDPR and the UK GDPR in this regard).

### 4.3 Legal obligation

Under Art. 6(1)(c), personal data can be processed when the processing *"is necessary for compliance with a legal obligation."* For example, a bank can process its customers' personal data to fulfill its obligations under anti-money laundering regulations.

Art. 6(3) further specifies that the source of a legal obligation must be EU or Member State law. The notion of law is broad and includes rules such as administrative acts or judicial decisions[^10]. Regardless, this "law" must fulfill specific requirements laid out by the GDPR. This means that Member States cannot make any processing of personal data lawful by simply creating a law for that purpose.

Much like the performance of a contract, legal obligation is a relatively hassle-free ground but is also very restrictive regarding what data can be processed.

### 4.4 Vital interest

Under Article 6(1)(d), data can be processed to protect the vital interests of the data subject or of another person. For example, if an employee is in imminent danger, the employer can provide the public force with GPS data from the company's care so that they can find them and take action as soon as possible.

In this context, *vital interest* means a life-threatening situation is taking place. This is a rather exceptional ground and not something you would use for day-to-day data processing.

### 4.5 Public interest or exercise of a public authority

This is a long one: under Art. 6(1)(e), data can be processed when it is *"necessary for the performance of a task carried out in the public interest or in the exercise of official authority vested in the controller."* For instance, a public school can process student grades based on its public task to further education. The tax authority can process your personal data when performing an inspection because they can do so under the law.

This ground is typically used by public authorities and public entities, as it is more flexible than legal obligation. It can also be used by private entities, but only in specific scenarios- for example when a private company provides a public service under a procurement contract.

Finally, the right to object we mentioned earlier also applies to the processing of data based on public interest/authority[^11].

## Final Thoughts

Handling personal data correctly is important. Still, guidelines and laws are not always easy to understand GDPR. We tried to create a comprehensive overview to give a bit more clarity on the different legal bases for data collection. The GDPR has set the boundaries for what's possible and what is not. As a business, you must adhere to these laws to protect your customer's privacy. Having a clear understanding of these legal bases reduces your company's risks of lawsuits and data breaches.

Even if the GDPR did not exist and there were no laws to violate concerning data protection, organizations are morally obliged to handle the data of their website visitors in a responsible manner. At least, this is what we believe at [Simple Analytics](https://www.simpleanalytics.com/).

This is why we created a privacy-first Google Analytics alternative that doesn't use cookies or collect personal data while still obtaining actionable insights from your [website visitors](https://simpleanalytics.com/simpleanalytics.com).

We believe in creating an independent web that is friendly to website visitors while providing the insights you need to run your business. If this resonates with you, feel free to [give us a try](https://simpleanalytics.com/welcome).

> [^1]:  This is the lawfulness principle laid out by Art. 5(1)(a) GDPR.
> [^2]:  Art. 4(11) GDPR.
> [^3]:  Public entities usually enjoy some degree of power imbalance with the data subject, meaning consent is not always freely given as required by Art. 4(11) GDPR. Art. 6 also provides that public authorities (which is more specific than public entities) cannot rely on legitimate interest when they could rely on public interest/authority instead.
> [^4]:  This is the three-part test developed by the CJEU (CJEU - C‑13/16 - Rīgas satiksme).
> [^5]:  See Art. 5(2) (accountability) as well as 24 GPDR (responsibility of the controller).
> [^6]:  If you want to know more about legitimate interest, the UK ICO provides some very accessible information on its [website](https://ico.org.uk/for-organisations/guide-to-data-protection/guide-to-the-general-data-protection-regulation-gdpr/legitimate-interests/what-is-the-legitimate-interests-basis/).
> [^7]:  Art. 6(1) GDPR.
> [^8]:  21 GDPR. The same goes for processing based on 6(1)(e).
> [^9]:  21(3) GDPR.
> [^10]: Kuner and others, Commentary On The EU General Data Protection Regulation (GDPR). A Commentary, 2020, p. 333.
> [^11]: 21 GDPR.
