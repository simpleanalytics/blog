---
title: "9 ways to protect user data to be GDPR compliant"
author_slug: carlo
author: Carlo Cilento
excerpt: "Data breaches are a risk for every company, so processing data in a secure and confidential way is critical for businesses"
image: https://assets.simpleanalytics.com/blog/2023-9-ways-to-protect-user-data/social-image-9-ways-to-protect-user-data.png
image_no_text: https://assets.simpleanalytics.com/blog/2023-9-ways-to-protect-user-data/social-image-no-text-9-ways-to-protect-user-data.png
related_posts:
  - /blog/why-its-time-to-move-away-from-google-analytics
  - /blog/website-analytics-without-cookies
  - /blog/is-google-analytics-illegal-in-europe
  - blog/is-google-analytics-4-gdpr-compliant
---

Protecting user data is not just an element of good data governance: it’s a legal duty under the GDPR. Data breaches can cost companies a fine and hurt their reputation, so processing data in a secure and confidential way is critical for businesses.

Of course there is no catch-all solution to ensure data security, as processing operations differ wildly from organization to organization. However, some basic guidelines apply to all scenarios. We are going to take technical security measures for granted (hopefully you are using secure authentication mechanisms, encrypting data, and so on) and focus on what can be done from a data governance perspective.

{% include gif.html slug="good-government-matters" alt="good government matters" width="500" height="357" color="#665247" %}

{{tableofcontents}}

Let’s dive in

## Know your data flows

The starting point for protecting user data is **good data governance**, which requires **knowing what you are doing with the data**. This might seem like a trivial point, but it isn’t. Data flows are often more complex than it appears at a glance: it’s easy to focus solely on the data you care about and overlook other categories of data that are also processed along with the “main” data.

For example, let’s say the legal department of a company stores copies of physical contracts with the customers in its filing system. This operation is more complex than it seems. Access credentials for the filing system are needed, and a system administrator will need to manage access privileges. Additionally, the company will definitely want to monitor access to the data, which means that the filing system should generate and store metadata for each user. Focusing too much on the CVs makes it easy to lose sight of the bigger picture.

[Data protection flows](https://assets.simpleanalytics.com/blog/2023-9-ways-to-protect-user-data/social-image-9-ways-to-protect-user-data.png)

Things are likely to be more complicated in real life: other staff members might enjoy different access privileges, the IT staff might need access to the system to do their jobs, third-party processors might be involved, and so on. Accounting for all of these variables is not simple, especially when dealing with complex data architectures.

Mapping out data flows has many benefits. An accurate and comprehensive map:

- highlights issues with access and security that you can address
- highlights opportunities to make your data architecture more efficient
- helps implement new data flows in a coherent way within the existing architecture
- helps ensure your access policy reflects the way data are actually processed
- makes it easier to keep a record of your processing activities (a requirement for some companies under the GDPR[^1])
- helps you comply with access and erasure requests because you know what data you control and where to find it within your systems.

Mapping data flows can be complicated for large businesses where different teams process. Other categories of personal data include customer data, web analytics data, employee data, payment information, etc. A company's data architecture also becomes increasingly complex over time, so the later you map it out, the harder it will be. Ideally, maps should be drafted from the start and periodically updated.

Meta’s case is quite instructive. Litigation against the company revealed that [no one at Meta knows exactly how data are processed](https://www.iccl.ie/news/unsealed-court-documents-reveal-data-anarchy-at-meta/). Facebook has been around for nearly two decades, but Meta only attempted (and failed) to map its data flows last year following a court order. Meta’s data architecture is so insanely complex that mapping it from scratch is practically impossible.

## Know your processors

Many companies rely on a third party to process data in one way or another, whether it’s cloud storage, a Platform-as-a-Service, an email service provider, or a contractor entrusted with IT maintenance.

Under the GDPR, these parties are data processors and must sign a data processing agreement (DPA) with you. Be mindful that you may be held accountable for any damage your processor may cause by violating the GDPR[^2]- including breaches they may suffer!

Ensure you only rely on trusted processors with good data governance and strict disclosure policies. The same goes for any sub-processor involved (that is, any processor working for your processor). If feasible, in-house processing for certain categories of data should be preferred (for example, trade secrets and sensitive personal data such as medical information).

## Adopt a responsible access policy

As a rule of thumb, the more people can access the data, the more things can possibly go wrong. **Role-based access control** ensures that the data can only be accessed by the staff who actually need them. This is especially important for large companies with a complex structure: HR needs sick leave data about employees, and management and marketing don’t.

## Be careful with data transfers

You can transfer your data outside the EU/EEA under the GDPR. Still, some transfers are more complicated than others. Transfers to countries covered by an adequacy decision are straightforward and come with no compliance burden- although you will still need to ensure that any reliable processor receives the data.

Things get trickier when you can’t rely on an adequacy decision. We are not going to discuss data transfers in detail, but in a nutshell, transfers outside the EU/EEA come with some compliance burdens (such as standard contractual clauses). These burdens should not be approached as an exercise of the form: it is your duty as the data controller to ensure that whatever transfer mechanism you use provides sufficient protection in practice. This can be problematic regarding countries that allow for widespread surveillance, such as the US. This is the core issue of Google Analytics’ ongoing troubles with data transfers and the GDPR.

If you’re curious, you can read our [blog](https://www.simpleanalytics.com/en/blog/how-to-move-forward-with-data-transfers-between-the-eu-us) to learn more about the Google Analytics saga and data transfers in general.

## Train your staff

While some data leaks are the consequence of sophisticated hacking attacks, many are perpetrated through phishing, and others yet are the result of human errors. Investing in technical security is a no-brainer to keep data safe, but staff training is equally important. You don’t need to turn every employee into a privacy lawyer, but the staff handling personal data should know when they should or shouldn’t disclose it. And crucially, they should be able to ask a qualified staff member when unsure what to do.

## Account for human errors

People make mistakes. You should account for this and set up data processing to minimize the risk of human error. Ask yourself: what mistakes are the most likely to happen in my company? Is there any way I can prevent those mistakes?

For instance: an Italian hospital was recently fined for [leaking the email addresses of hundreds of neurology patients](<https://gdprhub.eu/index.php?title=Garante_per_la_protezione_dei_dati_personali_(Italy)_-_9779057>). How did that happen? An employee accidentally included the patients’ emails in the CC field instead of BCC while forwarding a newsletter (oops!). This kind of mistake is not unlikely when employees send dozens of emails daily. The data breach could have been avoided by setting the email client to use BCC as the default setting, requiring an extra step (such as user confirmation) to use CC.

## Adopt a sensible DSAR verification policy

Under the GDPR; a data subject can request the data controller to provide certain information about the processing of their data and to provide a copy of the data themselves[^3]. These requests are typically referred to as data subject access requests or DSARs. Dissatisfied requesters sometimes file a complaint with a data protection authority, so handling DSARs promptly and adequately is important.

However, companies need to know that DSARs can be abused to access other people’s data illegally. In other words, **fake DSARs are a phishing tool**\- and a very effective one too! If you fall for a fake DSAR, you will suffer a data breach, so you must ensure requests don’t come from an impersonator.

At the same time, companies must handle requests within a time limit[^4] while also facilitating the exercise of the requester’s rights[^5]. Reconciling all these obligations is not simple, and there is no one-size-fits-all solution. Each company should find a suitable middle ground based on its specific situation and the nature of the data they handle. But as a rule of thumb, you should opt for the least burdensome and invasive verification that is reliable enough in your case[^6]. For instance, if you get a DSAR from someone claiming to be a registered user of your website or company, you can require them to forward the request from the email they registered with. You could also include a button to forward a DSAR in the user’s personal area on your website (Instagram does this, for instance). Ideally, you should only require an ID or other personal information as a last resort.

## Have a disaster recovery policy for your data

When people think of data breaches, they usually think of data leaks: situations where personal data are viewed or copied by an unauthorized party. However, data loss also qualifies as a data breach under the GDPR[^7]. This means that any data security policy should include a disaster recovery plan for your data. Ideally, an organization will have a backup, whether a physical backup or a cloud-based disaster recovery service.

## Process fewer data

It goes without saying that the more data you process, the more things can potentially go wrong. In addition to the cost of operating and maintaining your data processing systems, processing data has inherent costs in terms of compliance burdens and compliance risks, and the more complicated your processing operations, the higher those costs are. You should always ask yourself: **do I** **really** **need these data**, or am I collecting them just because everyone in my industry is doing so?

Sometimes using fewer data is the best option. There is a lot to be said about the value a **data minimization mindset** can bring to your company- and we wrote about it [here](https://www.simpleanalytics.com/en/blog/less-is-more-data-minimization-can-help-your-business).

Needless to say, your company should also adhere to a **sensible data retention policy** and erase the data it doesn’t need anymore. Doing so is both a legal requirement under the GDPR[^8] and sound practice for data security- any data you don’t have is data you cannot leak.

## Final Thoughts

Good data governance and a privacy mindset can bring value to your company, and relying on privacy-friendly tools is a great start. This is also one of the pillars on which Simple Analytics is built. We believe that you can collect insights on your website visitors without needing any personal data at all. This allows you to get the insights you need, while being 100% GDPR-compliant. We believe in an independent internet that is friendly to website visitors. If this resonates with you, feel free to give us a [try](https://simpleanalytics.com/welcome)!

> [^1]: Art. 30 GDPR.
> [^2]: Art. 82(2) GDPR. The controller is exempt from liability when it had no responsibility in causing the damage (Art. 82(3)), but it bears the burden of proof- which is very risky in practice.
> [^3]: Art. 15 GDPR.
> [^4]: Art. 12(3) GDPR.
> [^5]: Art. 12(2) GDPR.
> [^6]: This is also the recommendation of the EDPB: see Guidelines 01/2022 on data subject rights - Right of access, par. 65.
> [^7]: Art. 4(12) GDPR.
> [^8]: Art. 5(1)(e) GDPR.
