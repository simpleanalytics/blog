---
title: "How to move forward with data transfers between the EU & US"
author_slug: carlo
author: Carlo Cilento
excerpt: "Everything you need to know about the do's and don't regarding data transfers under the GDPR"
image: https://assets.simpleanalytics.com/blog/2022-data-transfers-under-the-GDPR/social-image.png
image_no_text: https://assets.simpleanalytics.com/blog/2022-data-transfers-under-the-GDPR/social-image-no-text.png
related_posts:
  - /blog/why-its-time-to-move-away-from-google-analytics
  - /blog/why-simple-analytics-is-a-great-alternative-to-google-analytics
  - /blog/the-complete-overview-from-101-noyb-complaints-to-banning-google-analytics
  - /blog/website-analytics-without-cookies
---

Data transfers between the EU and the US are one of the most widely discussed issues in data protection law right now. Countless business and governmental agencies across Europe are somehow reliant on a US-based processor for their operations. Yet, these data transfers pose privacy risks that are hard, if not impossible, to mitigate.

We've already touched upon data transfers in a [blog](https://www.simpleanalytics.com/blog/the-complete-overview-from-101-noyb-complaints-to-banning-google-analytics) that sums up the long story behind the DPA decisions against Google Analytics. However, this time we're going to look at data transfers from a more general viewpoint and try to explain the legal issues at stake in more detail.

{% include gif.html slug="closer-look" alt="closer look" width="480" height="259" color="#35281d" %}

{{tableofcontents}}

## How do data transfers work under the GDPR?

The GDPR contains all sorts of rules to protect the data rights of individuals. But what happens when your data is transferred to a third country outside the EEA?

The GDPR contains a Chapter about data transfers specifically, consisting of seven Articles (44-50). These rules aim to ensure that personal data enjoys the **same level of protection** when transferred[^1].

In practical terms, a data transfer to a third country is only lawful when it relies on one of several mechanisms listed by the GDPR. To keep this short, we will focus on the ones that really matter in practice: **adequacy decisions and standard contractual clauses**.

### Adequacy decisions

Adequacy decisions are decisions by the **European Commission** that essentially **greenlight data transfers** to a specific country[^2]. Before taking an adequacy decision, the legal system of that country is examined in depth and ensures that it grants a sufficient level of protection[^3].

If you have an adequacy decision for the transfer you need, you are lucky. Adequacy decisions are an easy, hassle-free way to transfer data. However, they only cover a small number of countries.

Keep in mind that adequacy decisions are **not political decisions**. That is to say; the Commission is not free to declare a country adequate just because they like it or because they are a political ally; it must make sure that data transfers to that country are actually safe and must take some specific criteria into account. The Court of Justice can invalidate an adequacy decision for a country that doesn't satisfy these criteria, which happened twice for the U.S.

### Standard contractual clauses

When you can't rely on an adequacy decision, you will need another mechanism for data transfers. Article 46 lists six of them, but in practice, you will probably use **standard contractual clauses (SCCs)[^4]**.

SCCs are a set of standard clauses drafted by the European Commission[^5]. When someone is transferring data to a third country, they need to include these clauses in a **legally binding agreement** with the recipient. So SCCs ideally make a transfer safe by implementing data protection rules into a contract between the parties.

The main shortcoming of SCCs is that they **do not bind the recipient State**. For this reason, they provide little or no protection against State surveillance. This does not mean that SCCs cannot be used when dealing with "unsafe" countries. In that case, **"supplementary measures"** will be needed, as in the case of U.S. data transfers.

In other words, the controller needs to ensure that SCCs grant sufficient protection in practice, and if they don't, they must take extra steps to keep the data confidential. As we will see, this is very difficult when dealing with State surveillance.

### What about other mechanisms?

As we said, the GDPR provides transfer instruments other than SCCs and adequacy decisions[^6], but they are not frequently used in practice. Binding Corporate Rules (BCRs) are used to transfer data within branches of a corporation. However, large corporations typically prefer establishing separate companies in the EEA and controlling them through capital ownership (think of Google Ireland and Meta Ireland). Certifications and codes of conduct may gain traction in the future but are not widely used at the moment.

Crucially, **all these instruments suffer from the same issues as SCCs** when dealing with "unsafe" States because they do not bind the recipient State (legally binding instruments between public bodies are the exception, but private entities cannot rely on them).

![Data transfers under the GDPR](https://assets.simpleanalytics.com/blog/2022-data-transfers-under-the-GDPR/social-image-no-text.png)

## US data transfers. A long story short

To understand where we are now concerning US data transfers, we need to take a quick look at a decade-long story of legal battles.

### Schrems I

From 2000 to 2015, data transfers between the EU and the U.S. were covered by a data transfer agreement called **Safe Harbor**.

In 2013 American whistleblower Edward Snowden leaked confidential documents about the operations of the CIA and NSA. The revelations contained **records on bulk data collection operations** that targeted foreign nationals on a large scale and were based on Section 702 of the FISA act and Executive Order 12333.

Shortly after the Snowden revelations, Austrian citizen **Max Schrems filed a complaint against Facebook Ireland** before the Irish supervisory authority (DPC). He claimed that the transfer of his personal data to Facebook Inc. was unsafe and illegal because of the extent and pervasiveness of State surveillance in the US, as documented in the Snowden files.

In 2015 the case landed in the EU Court of Justice, which ruled in Schrem's favor and [**invalidated the Safe Harbor regime**](https://curia.europa.eu/jcms/upload/docs/application/pdf/2015-10/cp150117en.pdf).

### Schrems II

Schrems' case continued, and was referred to the CJEU a second time. In 2020 the Court ruled in favor of Schrems again. It invalidated the **Privacy Shield**, another framework for data transfers that replaced the Safe Harbor regime in between the two Schrems rulings.

The validity of SCCs as a transfer mechanism was also questioned in the case. The Court did not invalidate SCCs in the ruling. Still, it stated that **supplementary measures** were needed to protect data from surveillance practices in "unsafe" countries such as the U.S. In other words, the Court "spared" SCCs but also made them more complicated and burdensome to use.

Overall, the Schrems II ruling made data transfers to the U.S. much more complicated. **Companies can no longer rely on an adequacy decision** after the Privacy Shield was invalidated and need to use other instruments (typically SCCs) instead. They also need to implement **adequate supplementary measures** to counter the risk of State surveillance.

### The 101 complaints

Despite widespread panic about data transfers, most companies kept doing business as usual and transferring data to the US as if Schrems II didn't happen.

But right after the Schrems II ruling, noyb (a privacy NGO founded by Schrems) filed [101 complaints](https://noyb.eu/en/101-complaints-eu-us-transfers-filed) centered on data transfers. The complaints were filed before the DPAs of several Member States and target websites using U.S.-based services Google Analytics and Facebook Connect. These complaints are a strategic effort to get European DPAs to **apply the Schrems II ruling rigorously**.

The EDPB (short for European Data Protection Board, a European institution gathering all European DPAs) later created a **[task force](https://edpb.europa.eu/news/news/2020/european-data-protection-board-thirty-seventh-plenary-session-guidelines-controller_en)** for coordinating the approach of European DPAs to noyb's complaints. By the looks of it, the task force did a good job: **three DPAs upheld the complaints** against Google Analytics so far, and the Dutch DPA stated that they might follow along. In a [recent press release](https://www.datatilsynet.dk/english/google-analytics/use-of-google-analytics-for-web-analytics), the Danish DPA also embraced the same approach and declared the use of Google Analytics unlawful.

But the issue is bigger than GA. The reasoning that led to Google Analytics being banned from some Member States may someday lead to the ban of many other services, including cloud services which are practically indispensable for the European economy at the moment.

## Supplementary measures for data transfers

And now the one billion dollar question: what supplementary measures are effective against U.S. surveillance?

The EDPD suggested some solutions in their guidelines on supplementary measures, but they are few, and all have significant limitations. It should be noted that these are only general suggestions: there is no clear-cut answer to the question, as **safeguards need to be chosen and evaluated case by case**.

### Encryption

A fundamental distinction needs to be made between end-to-end encryption and other forms of encryption.

**End-to-end encryption can be an effective safeguard[^7]**. However, it also **limits** what can be done with the data. Some processing operations are more difficult on encrypted data, and others simply require access to some data in the clear. For example, the provider of an end-to-end encrypted email service needs to process the address of the sender and recipient in the clear to deliver the mail. This information is still personal data under the GDPR.

On the other hand, **non-end-to-end encryption is never an effective safeguard**. If the service provider holds a decryption key[^8], it can be required to hand it over under FISA along with the encrypted data. In other words, your data is in a safe, but the companies can be forced to hand over the key. This is why the Austrian, French and Italian DPAs all dismissed Google Analytics' data encryption as irrelevant when dealing with noyb's complaints.

To be perfectly clear, non-end-to-end encryption is still a useful **cyber security measure**, as it effectively protects against attacks. It just doesn't help with U.S. data transfers at all.

### Proxy servers

The French DPA has proposed proxy servers as an **effective safeguard** for using Google Analytics. They are, but they cannot be used for all data transfers. They are also **burdensome and expensive** to implement, as the [French DPA itself acknowledges](https://www.cnil.fr/en/google-analytics-and-data-transfers-how-make-your-analytics-tool-compliant-gdpr).

The idea is simple in theory: instead of sending the data directly to Google, you run it through a proxy server and filter out or anonymize all personal data before sending it to Google.

Here's the catch: you must host and run Google Analytics **on your own server**. This means you must maintain the server and manually keep the software up to date, on top of writing code to anonymize any personal data. This is way more complicated and expensive than paying for a GDPR-compliant alternative.

Additionally, this solution requires **complete control of the infrastructure**. This is not an attractive option for using cloud services since the main advantage of clouds is that you don't need any physical infrastructure, to begin with.

### Pseudonymization

The EDPB also suggests **pseudonymization[^9]**. In a nutshell, pseudonymization means that you can only transfer data that cannot be used to re-identify the data subject, even in combination with other data.

Pseudonymization is not anonymization under the GDPR, but it can definitely be a useful privacy measure. It can also be **hard to implement correctly**. Replacing identifiers with pseudonyms is not enough, as you may need to process and transfer a lot of other potentially identifying data. In some cases, proper pseudonymization of all the data you transfer will be impossible or make the processing practically useless.

The controller also needs to consider data linkage- that is, the possibility that someone may re-identify the data subject by combining the exported data with any other information they may possess. Evaluating the risk of re-identification is difficult when dealing with State surveillance because intelligence agencies gather a lot of information about a lot of people and are not transparent about the information they possess- that's their job after all.

![do you really need google analytics](https://assets.simpleanalytics.com/blog/2022-do-you-really-need-google-analytics/social-image-no-text.png)

## The risk-based approach

Some companies adopt a **risk-based approach** to data transfers. They essentially claim that a transfer is safe and lawful when there is a low enough probability that the transferred data will be subject to surveillance.

However, Chapter V of the GDPR **never refers to the notion of risk[^10]**, and the Schrems II decision never considers the likelihood of data being subject to surveillance. This is why the EDPB, the EDPS[^11], and the Austrian and Italian DPAs[^12] have **explicitly rejected** the risk-based approach.

To be perfectly clear: when transferring data, an exporter should assess whether the specific data they are exporting are subject to any "problematic" surveillance legislation in the first place. This question is necessary for evaluating data transfers and should not be confused with the risk-based approach that DPAs are currently rejecting.

The answer to this question will be "yes" for most (if not all) transfers because the scope of FISA appears to be quite broad in practice- as confirmed by the Snowden papers.

## Now what?

As we have seen, data transfers are quite the legal puzzle right now. Effective safeguards are very few and are not available at all for some transfers. At the same time, authorities are moving towards a stricter approach to data transfers.

Of course, **this is bigger than Google Analytics alone**. A strict stance on data transfer might make it unlawful to use many U.S.-based service providers, including cloud-based services, which are practically **irreplaceable** right now.

This is why data transfers are a very delicate issue. On the one hand, the privacy safeguards of the GDPR should not be undermined by data transfers. On the other hand, it's unreasonable to shift the burden of compliance on companies entirely. Forcing businesses to ditch GA in favor of other analytics tools is one thing. Expecting them to make do without Oracle or AWS is something else entirely.

This is why a **political solution** needs to be found at some point. The European Commission and the US Government are currently working on another **data transfer agreement**, and an executive order on data transfers from President Biden is expected shortly. However, the US has not changed its surveillance legislation since the Schrems II ruling, and without such changes, a new data transfer framework may not survive a **Schrems III ruling**.

Even if the issues regarding data transfers will continue in the foreseeable future, businesses can protect themselves by using EU alternatives to US cloud services.

The GDPR is here to protect the data of EU citizens. Adhering to the law should be a priority for every business. In addition, we feel companies should go further than just sticking to the law.

The internet will be a better place if organizations navigate their business without relying on privacy-invasive tooling like Google Analytics. It is the right thing to do from an ethical standpoint. This is why we built [Simple Analytics](https://simpleanalytics.com/simpleanalytics.com), a [privacy-first Google Analytics alternative](https://www.simpleanalytics.com/blog/why-simple-analytics-is-a-great-alternative-to-google-analytics) that is cookieless by design and does not collect any personal data while providing the insights you need.

We believe in creating an independent web that is friendly to website visitors. If this resonates with you, feel free to [give us a try](https://simpleanalytics.com/welcome).

> [^1]: Art. 44(2) GDPR.
> [^2]: Art. 45 GDPR.
> [^3]: Art. 45(2) GDPR
> [^4]: Art. 46(2)(c) GDPR.
> [^5]: Technically a DPA could draft its own SCCs and submit them to the Commission for approval (Art. 46(2)(d) GDPR). But in practice, when someone talks about SCCs, they always mean the ones from the Commission.
> [^6]: Art. 46 GDPR.
> [^7]: EDPB Recommendations 01/2020 on measures that supplement transfer tools to ensure compliance with the EU level of protection of personal data, Version 2.0, par. 84.
> [^8]: EDPB Recommendations 01/2020 on measures that supplement transfer tools to ensure compliance with the EU level of protection of personal data, Version 2.0, par. 81.
> [^9]: EDPB Recommendations 01/2020 on measures that supplement transfer tools to ensure compliance with the EU level of protection of personal data, Version 2.0, par. 85.
> [^10]: The GDPR does adopt a risk-based approach to some compliance obligations (for example, security obligations under Art. 32 GDPR) but that is not the case with data transfers.
> [^11]: EDPB-EDPS Joint Opinion 2/2021 on standard contractual clauses for the transfer of personal data to third countries, par. 86 and 87.
> [^12]: The argument was not brought up before the French CNIL.
