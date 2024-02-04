---
title: "The Complete Overview: From 101 noyb complaints to banning Google Analytics"
author_slug: carlo
author: Carlo Cilento
excerpt: "A detailed overview of the current privacy issues with regard to data transfer to the U.S."
image: https://assets.simpleanalytics.com/blog/2022-complete-overview/noyb-text.png
image_no_text: https://assets.simpleanalytics.com/blog/2022-complete-overview/noyb-no-text.png
related_posts:
  - /blog/website-analytics-without-cookies
  - /blog/how-to-delete-google-analytics-in-4-steps
  - /blog/france-rules-google-analytics-to-be-in-conflict-with-gdpr-ruling
  - /blog/why-simple-analytics-is-a-great-alternative-to-google-analytics
---

2022 has been one hot year in data protection so far, with supervisory authorities ruling against Google Analytics left and right. We've tried our best to update you on all the current events, but even for us, it's hard to keep track of it. Here is an overview of the lengthy data transfer affair starting from Schrems II in 2020 until today. This is meant to provide a better understanding of where we are now and maybe catch a little glimpse of where we're headed.

{% include gif.html slug="its-a-lot" alt="its a lot" width="360" height="360" color="#494045" %}

{{tableofcontents}}

Let's dig in!

## Timeline

- July 2020: the CJEU issues the Schrems II preliminary ruling
- August 2020: noyb files the 101 complaints
- September 2020: the European Data Protection Board sets up a task force
- December 2021: decision from the Austrian DPA
- January 2022: decision by the European Data Protection Supervisor
- February 2022: decision from the French DPA
- June 2022: decision from the Italian DPA
- July 2022: Irish DPA announces draft decision suspending Meta Ireland's data transfers
- July 2022: German procurement authority holds U.S. data transfer unlawful
- July 2022: decision from the Danish DPA

## Data transfers in a nutshell

Before we dive into the Schrems II decision, we need some context. Under the GDPR, data transfers outside the EEA are only possible when personal data is adequately protected. This protection can be ensured in two ways:

1.  Transferring data to a third country covered by an 'adequacy decision.' This is a decision by the European Commission: the Commission evaluates the data protection rules in a third country and essentially greenlights data transfers to that country. Adequacy decisions are the easiest, most hassle-free mechanism for transferring data but have only been adopted for a limited number of countries.
2.  Through standard contractual clauses (SSCs) devised by the European Commission, which need to be incorporated in a legally binding agreement with the data processor. When transferring data based on SCCs, companies need to assess whether the clauses actually work in the third country. In other words, the data exporter cannot simply incorporate SCCs in the data processing agreement and call it a day but must ensure that the SCCs offer adequate protection in practice and implement additional safeguards when needed.

## Schrems II and Privacy Shield

An 'adequacy decision' was available for the U.S., based on a data transfer agreement known as Privacy Shield. However, in [Schrems II](https://gdprhub.eu/index.php?title=CJEU_-_C-311/18_-_Schrems_II), the Court of Justice ruled that the Privacy Shield did not ensure sufficient protection for personal data and invalidated the adequacy decision.

This left companies with SCCs as the only valid transfer mechanism for data to the U.S. However, the Court emphasized that additional safeguards for U.S. data transfers are needed when relying on SCCs: without such safeguards, transfers based on SCCs are illegal. Providing these safeguards for a US data transfer is no easy task, as many U.S. companies (including Google and Meta) are considered "electronic communication providers" under U.S. surveillance legislation. This means that they must comply with any request for data by the NSA.

Unfortunately, there is little a company can do to ensure adequate data protection in this scenario. Additionally, tech giants such as Google, AWS, and the like typically rely on standard, take-it-or-leave-it contracts for their business, leaving their customers with no room to negotiate additional safeguard clauses.

In this tricky scenario, some companies have adopted a risk-based approach: they essentially argue that their transfers are safe because the data they export is unlikely to be actually targeted by a FISA order- even though it may be theoretically possible. As we have seen, some Data Protection Authorities have started to reject this approach.

![complete overview of banning google analytics](https://assets.simpleanalytics.com/blog/2022-complete-overview/noyb-no-text.png)

## Noyb's 101 complaints and the EDPB task force

In the summer of 2020, right after the Schrems II judgment, noyb filed [101 complaints](https://noyb.eu/en/101-complaints-eu-us-transfers-filed) to various European supervisory authorities. Noyb is a privacy NGO chaired by Max Schrems (yes, the Schrems II guy). The 101 complaints are centered around data transfers and do not target Facebook or Google directly: they are directed against websites from online news outlets or commercial companies using either Meta or Google as data processors.

All complaints are similar in content and represent a strategy to nudge European DPAs (the Data Protection Authorities in each country) towards more rigorous enforcement of the GDPR concerning data transfers.

In a nutshell, websites use European companies Google Ireland/Meta Platforms Ireland as data processors, which in turn rely on their parent companies in the U.S. to process the data (that is, they are subprocessors in legal jargon). Noyb considers the data transfers between Google Ireland/Meta Platforms Ireland and their parent companies to be illegal under the GDPR and argues that companies should not be allowed to rely on services that require such transfers (such as Google Analytics).

In September 2020, the European Data Protection Board (EDPB) [announced the creation of a task force to handle noyb's 101 complaints](https://edpb.europa.eu/news/news/2020/european-data-protection-board-thirty-seventh-plenary-session-guidelines-controller_en). Few details about the works of the task force have been made public, but we do know that the DPAs worked towards finding a consistent approach to handling the complaints. The importance of this point cannot be stressed enough: the recent decisions that made the news reflect a coordinated approach, making it all the more likely that other supervisors will follow suit.

![do you really need google analytics](https://assets.simpleanalytics.com/blog/2022-do-you-really-need-google-analytics/social-image-no-text.png)

## Austria, France & Italy ban Google Analytics

The first decision on the 101 complaints came in December 2021 from the [Austrian DPA (DSB)](https://noyb.eu/en/austrian-dsb-eu-us-data-transfers-google-analytics-illegal). Two more complaints were upheld in 2022 by two of Europe's most influential and respected supervisors: the [French CNIL](https://www.cnil.fr/en/use-google-analytics-and-data-transfers-united-states-cnil-orders-website-manageroperator-comply) and the [Italian Garante](https://www.gpdp.it/web/guest/home/docweb/-/docweb-display/docweb/9782874#english).

The similarities between the decisions clearly reflect a common approach to the enforcement of Chapter V of the GDPR:

- The risk-based approach to data transfers was explicitly rejected.
- The additional safeguards implemented by Google were found to be insufficient. This includes (non-end-to-end) encryption of stored data, as the de-encryption keys were held by Google and could be requested by US agencies under a FISA order along with the targeted data.
- Google Analytics IP anonymization option was considered a form of pseudonymization rather than full anonymization. This means that the site's users' IP address is still regarded as personal data even when "anonymized" by Google.
- No fines were issued. DPAs are primarily looking to clarify that the rules on data transfers will be enforced more strictly in the future. Currently, they are not looking to punish companies as long as they take the supervisor's observations seriously and swiftly dismiss Google Analytics after the complaint is filed.

## EDPS reprimands European Parliament 

In January 2022, the European Data Protection Supervisor [reprimanded the European Parliament](https://gdprhub.eu/index.php?title=EDPS_-_2020-1013) for incorporating cookies from Google Analytics and Stripe (a payment company) into a website without informing the users and collecting their consent.

The site was an internal coronavirus testing website for Members of the European Parliament. The Parliament outsourced the development for the site, and the devs copy-pasted some of the code from another website they had developed, including unnecessary analytics functionalities.

The EDPS' decision only touched upon data transfers briefly, noting the complete lack of safeguards in this regard. However, it didn't draw as much attention as the 101 complaints.

## Ireland (DPC) orders Meta to suspend data transfers

In July 2022, the Irish DPA (DPC) announced a draft decision ordering [Meta Ireland to suspend transfers](https://www.simpleanalytics.com/blog/eu-moving-closer-to-facebook-ban) for their Facebook and Instagram services. The draft is the result of a lengthy investigation of the DPC. The draft is not publicly available, but the core issue of the decision is [the transfer of personal data based on SCCs](https://www.politico.eu/article/europe-faces-facebook-blackout-instagram-meta-data-protection/amp/).

[The Meta case is far from over](https://noyb.eu/en/one-month-european-dpas-decide-facebooks-eu-us-data-transfers). The decision is part of a complex procedure involving the EDPB, and other European DPAs may raise objections, further delaying the process. However, the announcement is still quite meaningful.

Many US companies (including Meta and Google) have their European establishment or spin-off companies in Ireland, and the Irish DPA is somewhat lax in policing them. An order to suspend transfers from a notoriously soft supervisor might signify an upcoming era of stricter enforcement of the transfer rules in the GDPR, which may concern countless services and companies- including Google and Google Analytics.

## The Procurement Chamber Baden-Württemberg

Another interesting case was decided in July 2022. The case was about a public procurement procedure for a digital management software. The winning company would rely on AWS Europe (Amazon Web Service EMEA SARL) as processors. While the data was entirely localized in the EU, U.S. parent company AWS Inc. could access personal data in order “to maintain and provide the service” and “to comply with the law or a valid and binding order of a governmental body”.

The Procurement Chamber found that this disclosure constituted a data transfer under the GDPR. The Chamber also found the data transfer to be illegal, as the additional safeguards in place were found to be lacking and SCCs on their own did not ensure sufficient protection.

The decision itself is far from clear. The deciding authority is not a data protection authority, nor is it typically involved in interpretation of the GDPR. Very important points of the decisions are barely touched upon, leaving it to the reader to infer the reasoning. That being said, this decision might be a sign that a hard stance on data transfers is starting to get traction outside the narrow boundaries of data protection law in a strict sense, and gaining momentum in the broader legal landscape.

![Caption of the image](https://assets.simpleanalytics.com/blog/2022-denmark-bans-google-products/denmark-bans-google-products-no-text.png)

## The Danish DPA's decision

The last chapter of the story so far is a [decision by the Danish DPAs](https://www.simpleanalytics.com/blog/denmark-bans-google-workspace-for-municipalities) (Datatilsynet). In July 2022, [the supervisor prohibited the municipality of Helsingør from using Google Workspace in schools](<https://gdprhub.eu/index.php?title=Datatilsynet_(Denmark)_-_2020-431-0061>). While the DPA highlighted several privacy concerns, data transfers were the main focus of the decision.

The processing operations involved both parent company Google LLC and Irish-based company Google Cloud EMEA Ltd. In the case at hand, the municipality was using a data localization setting available on Google Workspace. As a result, all data was stored in European servers by Google Cloud EMEA, and Google LLC was only involved in technical support. However, for Google LLC to provide support, Google Cloud EMEA would transfer data under SCCs, including personal data accessible in clear text. The DPA found this transfer to lack adequate safeguards and prohibited it.

The DSB warned that the same conclusions would likely apply to other municipalities using Google Workspace. The supervisor is handling these cases at the time of writing, and similar decisions will likely follow.

Notably, the case did not involve Google Analytics, and the Danish DPA was not involved in the 101 complaints at all. The decision might be a sign that the hard-line approach that started with the 101 complaints is gaining traction in other cases as well. If that were the case, this would be way bigger than "banning Google Analytics."

## The negotiations over the data transfer agreement

Currently, [the European Commission and the U.S. are negotiating a new agreement for data transfers](https://iapp.org/news/a/eu-us-agree-in-principle-to-new-transatlantic-data-agreement/). Such a deal will likely be challenged in the Court of Justice.

With no legal document available, it's hard to predict the result of a possible "Schrems III" ruling. But we know that the U.S. is not working on legislative reform of State surveillance - in fact, [the first federal privacy bill has been proposed in Congress](https://www.politico.com/news/2022/06/03/bipartisan-draft-bill-breaks-stalemate-on-federal-privacy-bill-negotiations-00037092) at the time of writing, and the draft does not limit the surveillance powers of the NSA under FISA. Without legislative reform, the agreement will likely not withstand the scrutiny of the Court of Justice.

## Final Thoughts

The enforcement system of the GDPR is a complex mechanism involving several actors: national supervisors, the EDPB, the national Courts of Member States, and the EU Court of Justice. Predicting the future direction of GDPR enforcement is no easy task, but all the signs seem to point in one direction. An era of strict enforcement of the rules on data transfers is likely coming, and it's time to prepare to stay ahead.

The recent decisions by EU members (France, Austria, and Italy) are part of a coordinated approach. For this reason, we expect more EU members to follow suit.

Organizations must adapt and be ready to navigate their business in this changing business environment. They must figure out what datapoints they really need to make decisions and collect them ethically. It's possible, and you'll be surprised how much data is collected for the sake of data collection.

We believe it's not only a matter of staying within the law. It goes beyond that. We believe in creating an independent web that is friendly to website visitors. That's why we built [Simple Analytics](https://simpleanalytics.com/simpleanalytics.com) without any tracking mechanisms or the ability to collect any personal data while still giving you the insights you need. If this resonates with you, feel free to [give us a try](https://simpleanalytics.com/welcome).
