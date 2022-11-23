---
title: "France directs schools to stop using Microsoft Office & Google Workspace"
author_slug: carlo
author: Carlo Cilento
excerpt: "the French Minister of Education clarified that French schools should not use Microsoft 365 and Google Workspace"
image: https://assets.simpleanalytics.com/blog/2022-
image_no_text: https://assets.simpleanalytics.com/blog/2022-
related_posts:
 - /blog/website-analytics-without-cookies
 - /blog/why-simple-analytics-is-a-great-alternative-to-google-analytics
 - /blog/how-to-delete-google-analytics-in-4-steps
 - /blog/google-analytics-performance-impact-using-google-lighthouse
draft: true
---

In a recent [response](https://questions.assemblee-nationale.fr/q16/16-971QE.htm) to an interrogation by a Member of the Parliament, the French Minister of Education clarified that **French schools should not use Microsoft 365 and Google Workspace**.

The reasons behind the Ministry's position are twofold. First, the Ministry is concerned about the **confidentiality and lawfulness of data transfers**. Second, reliance on European providers is coherent with the government's **"cloud at the center" policy**. Let's unpack all of this.

{% include gif.html slug="non-non-non" alt="non non non" width="480" height="270" color="#423e5c" %}

1.  [The privacy issues](#1-the-privacy-issues)
2.  [Digital sovereignty](#2-digital-sovereignty)
3.  [Final thoughts](#3-final-thoughts)

*Note: Some of the links below are in French, as the news didn't get much international media coverage*

## 1.  The privacy issues

The privacy concerns raised by the use of Google Workspace are nothing new. As we explained [here](https://www.simpleanalytics.com/blog/how-to-move-forward-with-data-transfers-between-the-eu-us#2-us-data-transfers-a-long-story-short), personal data of foreign citizens can be subject to invasive State surveillance when transferred to the US. These privacy concerns led the EU Court of Justice to **invalidate two frameworks for EU-US data transfers** in the landmark Schrems I and II decisions. It is worth noting that the Minister explicitly mentioned Schrems II in his response.

The Schrems II ruling has far-reaching implications for European companies. In principle, data can still be transferred to the US without a data transfer framework. However, the CJEU clarified that European companies must ensure the confidentiality of data transfers by **implementing adequate safeguards against State surveillance**. In practical terms, this is hard to do and entirely impossible for certain cloud-based services (we wrote about this [here](https://www.simpleanalytics.com/blog/how-to-move-forward-with-data-transfers-between-the-eu-us#3-supplementary-measures-for-data-transfers)).

In the aftermath of Schrems II, four European DPAs (the Austrian [DSB](https://gdprhub.eu/index.php?title=DSB_(Austria)_-_2021-0.586.257_(D155.027)), the French [CNIL](https://gdprhub.eu/index.php?title=DSB_(Austria)_-_2021-0.586.257_(D155.027)), the Italian [GPDP](https://gdprhub.eu/index.php?title=Garante_per_la_protezione_dei_dati_personali_(Italy)_-_9782890), and, more recently, the Hungarian [NAIH](https://gdprhub.eu/index.php?title=NAIH_(Hungary)_-_NAIH-3561-4/2022)) **ruled against the use of Google Analytics**. The tool requires data transfers between Google Ireland Ltd. and Google LLC. In line with the Schrems II ruling, the DPAs found these data transfers to be unlawful because they lacked effective safeguards against US surveillance. DPAs [coordinated their approach to data transfer complaints at a European level](https://edpb.europa.eu/news/news/2020/european-data-protection-board-thirty-seventh-plenary-session-guidelines-controller_en), so other DPAs are likely to follow suit. But the problem is more extensive than Google Analytics: other US services may come under fire next.

The CNIL is one of the DPAs that ruled against Google Analytics. By taking a strong stance on the use of Microsoft 365 and Google Workspace, the French government **embraced the CNIL's position** on data transfers. But this is not just about privacy.

## 2.  Digital sovereignty

Since last year, the French government has been pushing the **"cloud at the center" doctrine**: a long-term plan for developing digital infrastructure in the pursuit of **digital sovereignty**.

Last year, a circular from the Inter-departmental Directorate of Digital Affairs (DINUM) [urged public administration to ditch Microsoft 365](https://cloud-computing.developpez.com/actu/318885/La-DINUM-estime-que-Microsoft-365-n-est-pas-conforme-a-la-strategie-Cloud-au-centre-de-l-Etat-Francais-dans-une-circulaire-adressee-aux-secretaires-generaux-des-ministeres/) and use the on-premise Office suite instead. Privacy concerns played a role, but the government also aims to **limit France's reliance on US providers** in the long run. The Ministry's position on Microsoft 365 and Google Workspace falls squarely within this digital strategy.

It should be noted that Microsoft 365 does not require any data transfers outside the EU, as Microsoft processes all European data in European data centers. In the view of the Directorate, this is not enough to keep the data confidential. In fact, the Directorate urged administrations to **only rely on certified, EU-based cloud providers** that are guaranteed to be immune from the application of non-EU law (such as the US' controversial Cloud Act).

France is not alone in pushing toward digital sovereignty: [the EU digital strategy](https://ec.europa.eu/info/strategy/priorities-2019-2024/europe-fit-digital-age_en) acknowledges digital sovereignty as a key goal. And to lessen reliance on US-based service providers, the European Commission started [Gaia-X](https://gaia-x.eu/what-is-gaia-x/). This project brings together software and physical infrastructure providers to **create a secure data-sharing environment** under interoperable technical standards. Gaia-x aims to foster the growth of the digital economy across the Union, facilitate the sharing of data, and further the goal of digital sovereignty.

The potential implications of a data sovereignty policy should not be overlooked. Providing companies with competitive EU-based alternatives to US providers can help keep more data within the Union, where data protection rights can be **enforced more easily**. And lessening the dependency on US-based services would allow the **EU better leverage** when negotiating international data transfer frameworks.

## 3.  Final thoughts

The EU Digital Strategy and Gaia-X are a step in the right direction, but the Union still has a long way to go. At the present moment, some US providers are practically irreplaceable.

Fortunately, this is not the case for [Simple Analytics](https://www.simpleanalytics.com/). Unlike Google, we believe in creating an independent web that is friendly to website visitors. If this resonates with you, feel free to [check us out](https://simpleanalytics.com/simpleanalytics.com).
