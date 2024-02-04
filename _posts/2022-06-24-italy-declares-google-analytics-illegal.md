---
title: "Italy declares Google Analytics illegal"
author_slug: iron
author: Iron Brands
excerpt: "The Italian data protection authority declared the use of Google Analytics in violation with GDPR law"
image: https://assets.simpleanalytics.com/blog/2022-italy-bans-google-analytics/social-media.png
image_no_text: https://assets.simpleanalytics.com/blog/2022-italy-bans-google-analytics/social-media-no-text.png
related_posts:
  - /blog/why-its-time-to-move-away-from-google-analytics
  - /blog/the-complete-overview-from-101-noyb-complaints-to-banning-google-analytics
  - /blog/simple-analytics-easy-website-analytics-for-business-owners
  - /blog/why-its-time-to-move-away-from-google-analytics
last_modified_at: 2022-11-29
---

Italy has become the third country to rule against the use of Google Analytics officially. The news broke today after a careful examination concluded that Google Analytics violated GDPR law. You can find the statement [here](https://www.gpdp.it/web/guest/home/docweb/-/docweb-display/docweb/9782874#english).

<details markdown="1">
<summary>See the full article here</summary>

> ## Italian SA bans use of Google Analytics
>
> ### No adequate safeguards for data transfers to the USA
>
> A website using Google Analytics (GA) without the safeguards set out in the EU GDPR violates data protection law because it transfers users' data to the USA, which is a country without an adequate level of data protection.
>
> The Italian SA came to this conclusion after a complex fact-finding exercise it had started in close coordination with other EU data protection authorities following complaints it had received. The Italian SA found that the website operators using GA collected, via cookies, information on user interactions with the respective websites, visited pages and services on offer. The multifarious set of data collected in this connection included the user device IP address along with information on browser, operating system, screen resolution, selected language, date and time of page viewing. This information was found to be transferred to the USA. In determining that the processing was unlawful, the Italian SA reiterated that an IP address is a personal data and would not be anonymised even if it were truncated – given Google’s capabilities to enrich such data through additional information it holds.
>
> Based on the above findings, the Italian SA adopted a decision, to be followed by additional ones, [reprimanding](https://www.gpdp.it/garante/doc.jsp?ID=9782890) Caffeina Media S.r.l. – a website operator – and ordering it to bring the processing into compliance with the GDPR by ninety days. This deadline was considered to be appropriate in order to allow the operator to implement adequate measures in connection with the data transfer; if this is found not to be the case, suspension of the GA-related data flows to the USA will be ordered.
>
> The Italian SA highlighted, in particular, that US-based governmental and intelligence agencies may access the personal data being transferred without the required safeguards; it pointed out in this regard that the measures adopted by Google to supplement the data transfer instruments did not ensure an adequate level of protection for users’ personal data in the light of the guidance provided by the EDPB through its Recommendations No 1/2020 of 18 June 2021.
>
> The Italian SA wishes to draw the attention of all the Italian website operators, both public and private, to the unlawfulness of the data transfers to the USA as resulting from the use of GA – partly on account of the many alerts and queries received so far. The Italian SA calls upon all controllers to verify that the use of cookies and other tracking tools on their websites is compliant with data protection law; this applies in particular to Google Analytics and similar services.
>
> Upon expiry of the 90-day deadline set out in its decision, the Italian SA will check that the data transfers at issue are compliant with the EU GDPR, including by way of ad-hoc inspections.
>
> Rome, 23 June 2022

</details>

This news only comes a week after CNIL (French Data Protection Agency) [published guidelines](/blog/cnil-update-google-analytics-is-still-illegal) on the Google Analytics matter. These guidelines resulted from the statements made earlier this year in which [CNIL banned the use of Google Analytics](/blog/france-rules-google-analytics-to-be-in-conflict-with-gdpr-ruling).

More and more authorities are ruling against Google Analytics. This is not surprising: European data protection authorities **coordinated their approach** to cases involving Google Analytics’ data transfers. With coordination at a European level and the influential French and Italian DPAs leading the way, **we expect more authorities to follow the example**. _(Update: and the Hungarian DPA did)._

{% include gif.html slug="oh-my-god" alt="oh my god" width="480" height="400" color="695957" %}

{{tableofcontents}}

Let's dive in!

## Is Google Analytics really illegal in Italy?

In theory, no. In practice, yes.

The GPDP did not exactly say that you cannot use Google Analytics. It only forbids a specific website from doing so.

So what is all the fuss about? Well, the GPDP's decision highlighted a **lack of safeguards** in the data transfers which are required to run Google Analytics. In theory, a different website could implement better safeguards and use Google Analytics in a GDPR-compliant way. **But in practice, no website is positioned to do so** (as we explained [here](https://www.simpleanalytics.com/blog/how-to-move-forward-with-data-transfers-between-the-eu-us#3-supplementary-measures-for-data-transfers)).

So while the ruling does not technically ban Google Analytics, **it sets a precedent that practically amounts to a State-wide ban**. The same goes for every decision so far. In practical terms, Google Analytics is banned from Austria, France, and Italy (edit: and now Hungary too).

Privacy professionals and marketers are well aware that the recent decisions against Google Analytics practically amount to declaring it unlawful. This is why the rulings have drawn so much media attention.

![Italy bans Google Analytics](https://assets.simpleanalytics.com/blog/2022-italy-bans-google-analytics/social-media-no-text.png)
_The next domino is falling, Italy bans Google Analytics_

## What did the GPDP say exactly?

An Italian news outlet _(caffeinamagazine)_ used Google Analytics. When Google Analytics processes data, the information is sent from Google Ireland to its parent company Google in the US. This data transfer is only lawful under the GPDR when the data protection rights of the user can be adequately protected. According to the Schrems II ruling, the data controller must implement **effective safeguards** to keep the data confidential against US surveillance.

The GPDP considered all the safeguards in place for the data transfers and found them **insufficient**. (Non-end-to-end) encryption is insufficient because Google holds the key and can be required to hand them over to State agencies. The contractual safeguards in place between Google Ireland and Google are insufficient without any technical measures. The GPDP also clarified that the user's IP address is personal data even when anonymized by Google because Google employs **very weak anonymization**.

None of this is new. In fact, the GPDP is only repeating what the Austrian and French DPAs already clarified, and all authorities simply apply the criteria laid out by the **Schrems II judgment**.

## The issue with data transfers

But what makes data transfers to the US so problematic? Why do we need safeguards for them? Companies such as Google, Facebook, and AWS can be required to **hand over personal data of foreigners to US agencies** under US law (FISA Section 702).

Google's privacy concerns are nothing new. In 2013, the **Snowden files** revealed that foreign citizens' personal data could be subject to invasive State surveillance when transferred to the US. [The Snowden revelations unlighted two broad intelligence collection programs (Upstream and PRISM) authorized under FISA](https://noyb.eu/en/project/eu-us-transfers). Concerns over the broad scope of FISA and the lack of effective remedies against US surveillance led the EU Court of Justice to **invalidate two data transfer frameworks** between the EU and the US in the landmark Schrems I and II decisions.

The 2020 Schrems II ruling has far-reaching implications for European companies. In principle, data can still be transferred to the US without any data transfer framework. However, the CJEU clarified that European companies must ensure the confidentiality of data transfers by **implementing adequate safeguards against State surveillance**. In practical terms, **this is hard to do and entirely impossible for certain cloud-based services** (we wrote about this [here](https://www.simpleanalytics.com/blog/how-to-move-forward-with-data-transfers-between-the-eu-us#3-supplementary-measures-for-data-transfers)).

In the aftermath of Schrems II, privacy NGO noyb filed [101 identical complaints against data transfers](https://noyb.eu/en/101-complaints-eu-us-transfers-filed) centered on the use of Google Analytics and Facebook Connect. The complaints involve all EU DPAs and constitute a **strategic effort** to nudge Europe towards stricter enforcement of the rules clarified in Schrems II.

As we said, DPAs [coordinated their approach to these complaints at a European level](https://edpb.europa.eu/news/news/2020/european-data-protection-board-thirty-seventh-plenary-session-guidelines-controller_en). As a result, three European DPAs (the Austrian [DSB](<https://gdprhub.eu/index.php?title=DSB_(Austria)_-_2021-0.586.257_(D155.027)>), the French [CNIL](<https://gdprhub.eu/index.php?title=DSB_(Austria)_-_2021-0.586.257_(D155.027)>), and now the Italian [GPDP](<https://gdprhub.eu/index.php?title=Garante_per_la_protezione_dei_dati_personali_(Italy)_-_9782890>)) _(update: and the Hungarian NAIH)_ **ruled against the use of Google Analytics**. In line with the Schrems II ruling, the DPAs found the data transfers from Google Ireland to Google LLC to be **unlawful** because they **lacked effective safeguards against US surveillance**.

## The French CNIL Q&A Guidelines on Google Analytics

In their Q&A last week, CNIL addressed all the questions raised after they announced Google Analytics to be illegal in February of this year. Since then, Google has suggested different approaches to making sure Google Analytics can be used safely within the E.U. law. However, CNIL concluded that it is technically impossible to use Google Analytics compliantly.

Google has suggested different solutions that were shut down by CNIL:

- IP anonymization is not a valid solution because Google could not demonstrate that anonymization takes place before transferring the data to the U.S.
- Data encryption is an ineffective safeguard because Google holds the keys and can be required to hand it over to State agencies.

The only solution the CNIL might be open to is the total anonymization of all personal data through a proxy server. This solution is expensive and burdensome for most companies. It also makes it **impossible to use cookies**, which severely limits the analytic capabilities of Google Analytics.

## Updates

> A lot has happened in the months following the GPDP decision, so here are some updates:
>
> - The GPDP decided on two more of the complaints, ruling against the use of Google Analytics again. This confirms what was obvious already: the first case set a crucial precedent, and any other cases will be decided accordingly. The second and third decisions were literally copy-pasted from the first.
> - The Hungarian NAIH joined the DSB, CNIL, and GPDP in ruling against Google Analytics.
> - the Danish DPA essentially embraced the same approach in a press release on the use of Google Analytics.
> - A new framework for EU-US data transfers is on the way. The new framework is still problematic in some respects and will undoubtedly face a challenge in Court. We're looking at yet another Schrems ruling, and it's hard to say how it will play out.
> - We wrote two blogs about [data transfers in general](https://www.simpleanalytics.com/blog/how-to-move-forward-with-data-transfers-between-the-eu-us) and [Google Analytics' troubles with data transfers](https://www.simpleanalytics.com/blog/the-complete-overview-from-101-noyb-complaints-to-banning-google-analytics). These contain more in-depth information on the topics.

## Final Thoughts

Before concluding, it might be worthwhile to summarize what we've seen:

- Multiple DPAs have ruled against Google Analytics so far
- DPAs follow a coordinated approach, and two influential DPAs lead the way. Other authorities are likely to follow (update: the Hungarian DPA did)
- Decisions are nearly identical and practically amount to a Statewide ban.

Also worth mentioning: **Consumers demand privacy**.

The business environment is changing, and you should ask yourself if you want to move with it or stick to old beliefs and practices.

Google is even moving away from its current version of Google Analytics by [sunsetting Universal Analytics](/blog/google-to-sunset-universal-analytics-in-2023) in favor of GA4. In a statement, they announced that privacy is one of the main drivers for the switch. Although GA4 is still not privacy-friendly, at least they acknowledge that the world is changing.

There are alternatives to Google Analytics that actually care about the privacy of your users. Simple Analytics is one of them, but before I tell you that we are the best, we've created an in-depth [comparison with other privacy-friendly alternatives](/blog/4-privacy-friendly-google-analytics-alternatives) to make your own decision.

We believe it's not only a matter of staying within the law. Yes, that's important too. But it goes beyond that. We believe you can still make decisions based on website data without needing to collect personal data or track individuals.

That's why we built Simple Analytics. To provide you with the insights you need while protecting the privacy of your users and being 100% GDPR compliant. If this resonates with you, feel free to [give us a try](https://simpleanalytics.com/welcome).
