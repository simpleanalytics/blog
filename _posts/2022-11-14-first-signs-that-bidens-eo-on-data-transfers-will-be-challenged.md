---
title: "First signs that Biden's EO on Data Transfers will be challenged"
author_slug: carlo
author: Carlo Cilento
excerpt: "Baden-Württemberg State Commissioner criticized Biden's Exectuve Order on Data Tranfers. Thereby implicating that a deal between the EU and US is still far away"
image: https://assets.simpleanalytics.com/blog/2022-bidens-eo-will-likely-be-challenged/social-image-bidens-eo-will-be-challenged.png
image_no_text: https://assets.simpleanalytics.com/blog/2022-bidens-eo-will-likely-be-challenged/social-image-bidens-eo-will-be-challenged.png
related_posts:
 - /blog/website-analytics-without-cookies
 - /blog/is-google-analytics-4-gdpr-compliant
 - /blog/how-to-delete-google-analytics-in-4-steps
 - /blog/is-google-analytics-illegal-in-europe
draft: true
---

In a recent [press release](https://www.baden-wuerttemberg.datenschutz.de/usa-eu-datentransfer-durchfuehrungsverordnung-us-praesident/) (German only), Baden-Württemberg State Commissioner for Data Protection and Freedom of Information Stefan Brink voiced his criticism over US President Joe Biden's executive order on data transfers.

To be clear, the Commissioner is not the data protection authority of Baden-Württemberg, and his positions don't necessarily reflect the authority's. He is, however, the first privacy institution in Europe to comment on the executive order, so his criticism is worth considering. But first of all, we will need some context.

{% include gif.html slug="hmmm" alt="hmmm" width="480" height="400" color="#91837f" %}

1. [The aftermath of Schrems II](#1-the-aftermath-of-schrems-ii)
2. [The new executive order](#2-the-new-executive-order)
3. [The DPO's press release](#3-the-dpos-press-release)

Let's find out!

## 1. The aftermath of Schrems II

We already wrote about data transfers extensively [here](https://www.simpleanalytics.com/blog/how-to-move-forward-with-data-transfers-between-the-eu-us), so here's the story in a nutshell. In 2020 the EU Court of Justice issued its landmark [Schrems II ruling](https://gdprhub.eu/index.php?title=CJEU_-_C-311/18_-_Schrems_II). This ruling made data transfers to the US tricky for EEA companies for several reasons.

Before the ruling, personal data could be transferred to the US based on a data transfer framework called **Privacy Shield**. The Court of Justice invalidated the framework in Schrems II, forcing companies to rely on different tools for lawfully exporting their data.

Most companies need to rely on **standard contractual clauses** (SCCs). SCCs are a set of legally binding clauses drafted by the European Commission, which must be incorporated into a legally binding contract with the data recipient. However, SCCs **do not bind the recipient State**. This is problematic: **US surveillance is at the heart of the Schrems case**, and SCCs cannot prevent the NSA from accessing European data.

The Schrems II ruling also dealt with SCCs and examined their validity as a mechanism for data transfer. The Court held that SCCs are a valid mechanism for data transfers even when dealing with "unsafe" States, on the condition that  the data controller implements effective **additional safeguards** to protect the data. In practice, **this is hard to do and entirely impossible for certain types of transfers**. So the Court essentially "spared" SCCs but made them much trickier.

After Schrems II, European data protection authorities have started taking a **harder approach** to data transfers. Three[ DPAs have essentially banned Google Analytics](https://www.simpleanalytics.com/blog/is-google-analytics-illegal-in-europe) (we wrote about this extensively), and the DPC announced a draft decision to [shut down data transfers for Meta Platforms Ireland](https://iapp.org/news/a/irish-dpc-files-draft-order-to-halt-metas-data-transfers-to-us/). These DPAs are following a coordinated approach[^1], so there is a real possibility that others will follow their example and that other US service providers will come under fire. This creates a climate of legal uncertainty around US data transfers.

## 2. The new executive order

Joe Biden's recent executive order is a first step towards a new framework called the **Trans-Atlantic Data Privacy Framework**. The order implements some material rules to limit the scope of surveillance and lays out a convoluted system for providing people in the EU[^2] with judicial remedies.

An **adequacy decision** by the European Commission will almost certainly follow in the upcoming months, essentially **greenlighting the US as a "safe" country** for data transfers. This will allow European companies to transfer personal data without the need to implement SCCs and additional safeguards.

Companies on both sides of the Ocean hope the new framework will bring legal certainty and allow for hassle-free data transfers. However, the future adequacy decision will surely come under scrutiny from the Court of Justice. Privacy NGO noyb [criticized the new framework](https://noyb.eu/en/new-us-executive-order-unlikely-satisfy-eu-law) and will likely challenge it in the **Court of Justice**.

## 3. The DPO's press release

In the upcoming months, the EDPB will issue an opinion on the matter as a part of the decision procedure for the adequacy decision. While the Board's opinion is not binding, it will give us better insight into the core issues of Schrems III.

In the meantime, the **Commissioner for Data Protection and Freedom of Information** for the German State of **Baden-Württemberg** has voiced some concerns over the new executive order. Interestingly, some of the issues raised by the Commissioner were also **highlighted by noyb** in a recent [press release](https://noyb.eu/en/new-us-executive-order-unlikely-satisfy-eu-law) (the same we linked above):

-   Individuals who file a complaint are given very little information about the decision. This can make decisions difficult to appeal in practice.
-   The Data Protection Review Court (which has the last word on any surveillance complaint) is a branch of the executive and not a part of the US judiciary system. It is unclear whether the CJEU will consider this Court to be independent.
-   The fact that the executive order mentions proportionality[^3] does not mean that the US surveillance system is, in fact, proportional, as the notion of proportionality may be interpreted differently by the Data Protection Review Court and by the EU Court of Justice.

The Commissioner also voiced other concerns. For instance, executive orders are **revocable at will** by the President, which makes them unsuitable for protecting individual rights. And it is yet unclear how the executive order will **interact with existing surveillance regulations**.

### Final thoughts

The executive order is very complex, and it will take a while for the privacy community to unpack it all. It's hard to say how a "Schrems III" case will play out, but it's clear already that the new framework is potentially problematic under several aspects. Overall, **the future of US data transfers is still unclear**.

We, [Simple Analytics](https://www.simpleanalytics.com/), will keep you updated on the matter through our [privacynewsletter](https://theprivacynewsletter.com/). If you want to be on the safe side, there are privacy-friendly and GDPR-compliant alternatives to Google Analytics. We are one of them. Feel free to check out what we are building [here](https://simpleanalytics.com/simpleanalytics.com). Unlike Google, we believe in creating an independent web that is friendly to website visitors. If this resonates with you, feel free to [give us a try](https://simpleanalytics.com/welcome).

> [1]: The decisions against Google Analytics are related to [101 complaints](https://noyb.eu/en/101-complaints-eu-us-transfers-filed) filed by NGO noyb over data transfers. The EDPB set up a [task force](https://edpb.europa.eu/news/news/2020/european-data-protection-board-thirty-seventh-plenary-session-guidelines-controller_en) to coordinate the DPAs' approach on a European level.
> [2]: The system will be accessible to anyone in the EU, because they enjoy data protection rights under the GDPR regardless of citizenship.
> [3]: Proportionality is a specific notion under EU law and played an important role in the Schrems II decision. In this context, and as a rule of thumb, you can think of a measure (such as State surveillance) as proportionate when it is both necessary for a legitimate purpose, and not excessive. See Art. 52(1) of the Charter of Fundamental Rights of the European Union.
