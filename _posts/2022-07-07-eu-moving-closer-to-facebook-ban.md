---
title: "EU moving closer to Facebook ban"
author_slug: carlo
author: Carlo Cilento
excerpt: "The Irish DPC concluded that it will block Facebook from sending data form the EU to the US"
image: https://assets.simpleanalytics.com/blog/2022-eu-moving-closer-to-facebook-ban/social-image.png
image_no_text: https://assets.simpleanalytics.com/blog/2022-eu-moving-closer-to-facebook-ban/social-image-no-text.png
related_posts:
 - /blog/website-analytics-without-cookies
 - /blog/less-is-more-data-minimization-can-help-your-business
 - /blog/vodafone-deutsche-telekom-to-introduce-persistent-user-tracking
 - /blog/new-ruling-your-cookie-data-might-be-sensitive-data-here-is-why-that-matters
last_modified_at: 2023-01-13
---

On Thursday, the Irish data protection authority (DPC) announced that they might stop data transfers between Meta Platforms Ireland and its US parent company, **effectively shutting down Facebook in Europe**.

<details markdown="1">
<summary>Read the full statement here by Politico.eu who were the first to report</summary>

> At July 7, 2022 12:37 PM CET by Vincent Manancourt.
> 
> Europeans risk seeing social media services Facebook and Instagram shut down this summer, as Ireland's privacy regulator doubled down on its order to stop the firm's data flows to the United States.
> 
> The Irish Data Protection Commission on Thursday informed its counterparts in Europe that it will block Facebook-owner Meta from sending user data from Europe to the U.S. The Irish regulator's draft decision cracks down on Meta's last legal resort to transfer large chunks of data to the U.S., after years of fierce court battles between the U.S. tech giant and European privacy activists.
> 
> The European Court of Justice in 2020 [annulled](https://curia.europa.eu/juris/fiche.jsf?id=C%3B311%3B18%3BRP%3B1%3BP%3B1%3BC2018%2F0311%2FJ) an EU-U.S. data flows pact called Privacy Shield because of fears over U.S. surveillance practices. In its ruling, it also made it harder to use another legal tool that Meta and many other U.S. firms use to transfer personal data to the U.S., called standard contractual clauses (SCCs). This week's decision out of Ireland means Facebook is forced to stop relying on SCCs too.
> 
> Meta has repeatedly warned that such a decision would shutter many of its services in Europe, including Facebook and Instagram.
> 
> "If a new transatlantic data transfer framework is not adopted and we are unable to continue to rely on SCCs or rely upon other alternative means of data transfers from Europe to the United States, we will likely be unable to offer a number of our most significant products and services, including Facebook and Instagram, in Europe," Meta [said in a filing to the U.S. Securities and Exchange Commission in March](https://d18rn0p25nwr6d.cloudfront.net/CIK-0001326801/c07375c5-b2dc-4223-8166-3365a3a1dbfd.pdf) this year.
> 
> The Irish blocking order, if confirmed by the [group of European national data protection regulators](https://edpb.europa.eu/edpb_en), is likely to send a chill through the wider business community too, which has been scratching its head about how to continue sending data from Europe to the U.S. following the EU's top court ruling in 2020.
> 
> The EU and U.S. are in the midst of negotiating a new data-transfer text that would allow companies like Meta to continue to ship data across the Atlantic irrespective of the Irish order. Brussels and Washington [in March agreed to a preliminary deal at the political level](https://www.politico.eu/article/eu-us-strike-preliminary-deal-to-unlock-transatlantic-data-flows/), but negotiations on the legal fine print have stalled and a final deal is unlikely to be reached before the end of the year.
> 
> A spokesperson for the Irish DPC confirmed that the draft decision had been sent to other European privacy regulators, who now have a month to give their input, but wouldn't discuss details of the decision.
> 
> "This draft decision, which is subject to review by European Data Protection Authorities, relates to a conflict of EU and U.S. law which is in the process of being resolved," a Meta spokesperson said. "We welcome the EU-U.S. agreement for a new legal framework that will allow the continued transfer of data across borders, and we expect this framework will allow us to keep families, communities and economies connected."
> 
> View source at [politico.eu](https://www.politico.eu/article/europe-faces-facebook-blackout-instagram-meta-data-protection/amp/).

</details>

The DPC drafted a decision to shut down Meta's data transfers for Facebook and submitted it to the European Data Protection Board  Data protection agencies from other EU Member States have a month to add their views and objections before it moves forward, but the process will likely take longer. The move could mean the biggest disruption of the social media giant in its history. The DPC did not disclose the contents of the draft.

Earlier this year, Facebook stated that if it's unable to transfer data overseas, it could affect the availability of its products. This scenario now seems close to becoming a reality now.

{% include gif.html slug="damn" alt="damn" width="480" height="270" color="#594542" %}

1. [Facebook and Schrems. A long story](#1-facebook-and-schrems-a-long-story)
2. [Crackdown on Google Analytics](#2-crackdown-on-google-analytics)
3. [Privacy Shield 2.0](#3-privacy-shield-20)
4. [Implications of Facebook ban](#4-implications-of-facebook-ban)

## 1. Facebook and Schrems. A long Story

The draft decision is the result of a long and complex legal battle between Max Schrems and Facebook. Nine years ago, privacy activist Max Schrems filed a complaint about Facebook’s data transfers before the DPC, citing privacy concerns in the wake of the Snowden revelations. The case ended up in the EU Court of Justice twice, and the Court invalidated two EU-US **data transfers frameworks** in the landmark Schrems I and II cases.

Schrems II made US data transfers tricky, as the Court highlighted the need to **implement effective safeguards against US surveillance**\- which is hard and often impossible for European companies.

Under US surveillance law, Facebook qualifies as an “Electronic communication service provider” and is therefore obliged to share data with the US intelligence service if requested. This means that US agencies can access the personal data of EU citizens. 

The mandate of the GDPR is simple: protecting the privacy of European data. This cannot be guaranteed when personal data is sent from the EU to Facebook servers in the US. 

## 2. Crackdown on Google Analytics 

The Schrems II ruling did not lead to a response from data protection authorities until the beginning of this year, when the [DSB (Austria)](https://noyb.eu/en/austrian-dsb-eu-us-data-transfers-google-analytics-illegal) responded by banning the use of Google Analytics. [CNIL (France)](https://www.cnil.fr/en/) was quick to follow, and [Garante (Italy)](https://www.gpdp.it/web/guest/home/docweb/-/docweb-display/docweb/9782874#english) banned Google Analytics last week as well (update: Hungary joined too). More EU member states are likely to follow suit in the coming months.

<img src="https://assets.simpleanalytics.com/blog/2022-eu-moving-closer-to-facebook-ban/social-image-no-text.png" alt="EU bans facebook" class="border-radius" />

## 3. Privacy Shield 2.0

A Facebook spokesperson noted that the issue is in the process of being resolved, referring to a new agreement between the U.S and the EU that will allow the continued transfer of data. The so-called Privacy Shield 2.0. However, the deal is far from finalized. Both the EU ([here](https://ec.europa.eu/commission/presscorner/detail/en/STATEMENT_21_1443)) and the US ([here](https://www.whitehouse.gov/briefing-room/speeches-remarks/2022/03/25/remarks-by-president-biden-and-european-commission-president-ursula-von-der-leyen-in-joint-press-statement/)) announced a new agreement on a new framework for transatlantic data transfer, but no legal document has been provided.

Max Schrems (yup, the one from the rulings) [noted](https://noyb.eu/en/privacy-shield-20-first-reaction-max-schrems):

> Update: the new framework for EU-US data transfers is on the way after US President Joe Biden signed an [executive order](https://www.whitehouse.gov/briefing-room/statements-releases/2022/10/07/fact-sheet-president-biden-signs-executive-order-to-implement-the-european-union-u-s-data-privacy-framework/) in October. The new framework is still problematic in some respects and will surely face challenges in Court. We’re looking at yet another Schrems ruling, and it’s hard to say how it will play out. Implications of Facebook ban.

## 4. Implications of Facebook ban

An unresolved conflict about transatlantic data transfer could have a significant impact on (almost) all Europeans. It sounds unrealistic that Facebook would not be available for EU citizens, but this might very well become a reality.

In February, [DPC head Helen Dixon told Reuters](https://www.reuters.com/technology/irish-regulator-moves-closer-possible-ban-facebook-instagram-eu-us-data-flows-2022-07-07/) that a decision would not immediately affect WhatsApp as it has a different data controller.

It sounds harsh, but finally, the GDPR is showing its teeth. Privacy is a human right and should be treated as such. Google and Facebook have become the biggest monopolies companies in the world by monetizing our data. This model is showing cracks as more and more consumers are demanding privacy.

## Final thoughts

We started Simple Analytics because we care about privacy. Our "fight" is mainly with Google as Simple Analytics is a privacy-first [Google Analytics alternative](https://blog.simpleanalytics.com/why-simple-analytics-is-a-great-alternative-to-google-analytics), but it goes further than that. We believe in an independent web that is friendly to website visitors.

To create a more open web, we need to adopt a different mindset. We must find ways to stop relying on the biggest advertising companies in the world. We really need to figure out how to become independent from those data-devouring beasts.

To change this, we need alternatives that allow us to do so. And yes, we are biased because we built a privacy-first Google Analytics alternative. But if this message resonates with you, you should check out all these [EU-based alternatives for digital products](https://european-alternatives.eu/) and see for yourself.
