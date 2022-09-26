---
title: "US data transfer unlawful according to German procurement authority"
author_slug: carlo
author: Carlo Cilento
excerpt: "German procurement authority rules US data transfer unlawful"
image: https://assets.simpleanalytics.com/blog/2022-us-data-transfer-unlawfull-germany/social-image.png
image_no_text: https://assets.simpleanalytics.com/blog/2022-us-data-transfer-unlawfull-germany/social-image-no-text.png
related_posts:
 - /blog/denmark-declares-google-analytics-unlawful
 - /blog/how-to-delete-google-analytics-in-4-steps
 - /blog/france-rules-google-analytics-to-be-in-conflict-with-gdpr-ruling
 - /blog/why-simple-analytics-is-a-great-alternative-to-google-analytics
---

On July 13, the Public Procurement Chamber of the German State of Baden-Württemberg decided a [case](https://gdprhub.eu/index.php?title=Datatilsynet_(Denmark)_-_2020-431-0061) about a public procurement procedure for a digital management software. In doing so, it held that personal data transfers to the US based on Standard contractual clauses violates the GDPR.

It should be noted that the Chamber is not a data protection authority and that the case is not, strictly speaking, a data protection case. However, the decision is quite significant. Several European DPAs have taken a strict approach to data transfers in handling the [101 complaints by noyb](https://noyb.eu/en/101-complaints-eu-us-transfers-filed). The decision at hand signals that the hardline approach to data transfers may now be gaining traction outside the narrow boundaries of data protection law.

In addition, the decision is mostly focused on the administrative law angle. The data protection issues at play are not explained very clearly and the Chamber’s reasoning on some crucial points needs to be inferred by the reader. This is not an easy decision to decipher, but we’ve done our best to present the gist of it in an accurate and readable way.

{% include gif.html slug="its-badass" alt="Its badass" width="500" height="326" color="#3f2e1f" %}

1.  [The case at hand](#1-the-case-at-hand)
2.  [The main points of the ruling](#2-the-main-points-of-the-ruling)
3.  [The consequences of the ruling](#3-the-consequences-of-the-ruling)

Let's dive in!

## 1. The case at hand

A public authority issued an invitation to tender for the procurement of software for digital management. The award criteria included data protection and security requirements: specifically, all data needed to be processed in compliance with the GDPR as well as federal data protection law. The bid was won by the EU subsidiary of a US company (the names of the companies are omitted).

Another company that took part in the tender asked the Chamber to examine the decision, claiming that the service offered by the winning company involved U.S. data transfers in violation of the GDPR. In fact, the winning company relied on AWS’s EU spin-off company (Amazon Web Services EMEA SARL) as a processor. AWS EMEA offered the option to store data in the EU, but would still disclose personal data to the parent company in specific scenarios:

1.  To maintain the service or provide support. 
2.  To comply with the law or a legally binding order.

Standard contractual clauses (SCCs) were the data transfer mechanism under the GDPR. As an additional safeguard measure, the company encrypted the data and assumed an obligation to challenge any “overboard or excessive” data access requests from authorities.

The Chamber held that the data transfer was indeed in violation of Chapter V GDPR. The public authority was ordered to re-evaluate the offers again, as compliance with the GDPR was one of the requirements set out in the tender notice. 

## 2. The main points of the ruling

- **SCCs do not ensure adequate protection** for personal data transfers to the U.S.
- **The additional safeguards were deemed insufficient** (but arguments about encryption were not considered by the Chamber for procedural reasons)
- **The mere accessibility of personal data from a U.S. provider means that a data transfer is in place** and that the GDPR rules on data transfers apply. In fact, the data were localized in the EU in the case at hand. Still, they could be accessed by the U.S. parent company(the case is somewhat similar to [the recent Datatilsynet decision on Google Workspace](https://www.simpleanalytics.com/blog/denmark-bans-google-workspace-for-municipalities) in this regard).

The reasoning behind this ruling is in line with the logic of multiple European DPAs and finds its merits in the fact that U.S. companies that qualify as an "electronic communication service provider." are obliged to disclose data to U.S. intelligence services if requested.

<img src="https://assets.simpleanalytics.com/blog/2022-german-authority-rules-US-data-transfer-unlawful/germany-gdpr.png" alt="german authority rules data transfer unlawful" class="border-radius" />
<p class="caption" markdown="1">
</p>

## 3. The consequences of the ruling

Some points need to be stressed. First, the Public Procurement Chamber is neither a data protection authority nor a court but rather an independent authority dealing with administrative law. Therefore, the decision will probably not carry as much weight as a decision from a DPA. Second, the Chamber is only competent with regard to the German State of Baden-Württemberg; other German authorities may endorse a different approach.

That being said, the decision is quite significant. The Public Procurement Chamber is not one of the central actors in enforcing the EU data protection framework and is typically not involved with the interpretation of the GDPR. However, the decision is consistent with the approach endorsed by several European DPAs when dealing with noyb’s 101 complaints (which is a result of the coordination efforts of the European Data Protection Board). This might be a sign that a hard-line approach to data transfers is gaining momentum and influencing authorities less involved in the enforcement of the GDPR.

## Final Thoughts

Privacy is a human right and should be treated as one. EU regulatory bodies are finally showing their teeth. For organizations that want to stay within the law, there are numerous European alternatives that could replace the US counterparts you are using now.

We built Simple Analytics as a privacy-first alternative to Google Analytics. We believe it's not only a matter of staying within the law. It goes beyond that. We believe in creating an independent web that is friendly to website visitors. That's why we built [Simple Analytics](https://simpleanalytics.com/simpleanalytics.com) without any tracking mechanisms or the ability to collect personal data while still giving you the insights you need. If this resonates with you, feel free to [give us a try](https://simpleanalytics.com/welcome).
