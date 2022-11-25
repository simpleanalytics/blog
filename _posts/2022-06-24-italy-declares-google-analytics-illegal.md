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
last_modified_at: 2022-09-20
---

Italy has become the third country to ban Google Analytics officially. The news broke today after a careful examination concluded that Google Analytics violated GDPR law. You can find the statement [here](https://www.gpdp.it/web/guest/home/docweb/-/docweb-display/docweb/9782874#english).

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

This news only comes a week after CNIL (French Data Protection Agency) [published guidelines](https://blog.simpleanalytics.com/cnil-update-google-analytics-is-still-illegal) on the Google Analytics matter. These guidelines resulted from the statements made earlier this year in which [CNIL banned the use of Google Analytics](https://blog.simpleanalytics.com/france-rules-google-analytics-to-be-in-conflict-with-gdpr-ruling).

It seems that more and more E.U. states are coming to the same conclusion: Google Analytics is illegal.

{% include gif.html slug="oh-my-god" alt="oh my god" width="480" height="400" color="695957" %}

1.  [Italy bans Google Analytics](#1--italy-bans-google-analytics)
2.  [CNIL Q&A guidelines on Google Analytics](#2--cnil-qa-guidelines-on-google-analytics)
3.  [Privacy Shield 2.0](#3--privacy-shield-20)
4.  [Is Google Analytics illegal?](#4--is-google-analytics-illegal)

Let's dive in!

## 1.  Italy bans Google Analytics

Italy is the third country to ban Google Analytics. This was concluded by Garante (the Italian Data Protection Authority) after a complex investigation in coordination with other European privacy authorities.

It reached the same conclusion as the DSB (Austrian Data Protection Authority), which was the first to rule the use of Google Analytics illegal. This has been the starting point for a chain reaction that led the French and now Italians to follow, and we'll see more in the coming months.

The problem here is the transfer of personal data to the United States. Google is a U.S. company that qualifies as an "electronic communication service provider." This means that Google is by law obliged to disclose data to U.S. intelligence services if requested.

The main reason for introducing the GDPR law in 2018 is to safeguard the privacy of E.U. citizens. The fact that Google transfers data to the U.S. and is obliged to hand it over upon request means the E.U. can no longer guarantee its citizens' privacy.

In declaring that the processing was unlawful, Garante stated that IP addresses were processed by Google and thus consisted of transferring personal data. Even if it were truncated, it would not become anonymous data, given Google's ability to enrich it with other data in its possession.

This is a very important nuance. It means that even if you anonymize IP addresses (like GA4 or Matomo), it's still considered personal data.

<img src="https://assets.simpleanalytics.com/blog/2022-italy-bans-google-analytics/social-media-no-text.png" alt="Italy bans Google Analytics" class="border-radius" />
<p class="caption" markdown="1">
  The next domino is falling, Italy bans Google Analytics
</p>

## 2.  CNIL Q&A Guidelines on Google Analytics

In their Q&A last week, CNIL addressed all the questions raised after they announced Google Analytics to be illegal in February of this year. Since then, Google has suggested different approaches to making sure Google Analytics can be used safely within the E.U. law. However, CNIL concluded that it is technically impossible to use Google Analytics compliantly.

Google has suggested different solutions that were shut down immediately by CNIL:

-   Anonymizing data is not a valid solution because Google could not demonstrate that it does this before transferring the data to the U.S.
-   Data encryption is invalid because if Google still holds the keys, they still have access.

CNIL also stated that a legal agreement between the E.U. & the U.S. is far from established.

## 3.  Privacy Shield 2.0

All of this has been kicked off by [Schrems II](https://iapp.org/news/a/the-schrems-ii-decision-eu-us-data-transfers-in-question/), which invalidated the privacy shield. The privacy shield meant that data transfers outside the E.U. were only possible if adequate safeguards were in place.

Schrems II invalidated this and made it painfully clear that these safeguards for data transfer to the U.S. were not in place. It took a while (1,5 years) for the first E.U. member states to take action to protect the privacy of their citizens. First the Austrian DSB, then the French CNIL, and now the Italian Garante.

After the DSB & CNIL declared the use of Google Analytics illegal, The E.U. and U.S. announced an agreement on a new framework for transatlantic data flow, known as the [Privacy Shield 2.0.](https://blog.simpleanalytics.com/eu-us-privacy-shield-2-0-is-again-a-political-show) However, it became apparent quickly that this agreement had zero legal merits. The announcement was meant as an 'agreement in principle.' It might take very long before a legal document is signed.

## 4.  Is Google Analytics illegal?

This is a broad question because it ultimately depends on where you live. This article covers the fact that the Italian Data Protection Authority publicly stated that using Google Analytics is illegal as long as the privacy shield is invalidated. The focus of the statement is on the use of Google Analytics. Still, the same conclusion would also hold for companies like Mailchimp or any other company that processes personal data and is marked as an “electronic communication service provider” by the U.S. government. 

To come back to the question of whether Google Analytics is illegal. We should narrow it down to whether Google Analytics is illegal in Europe. Italy, France, and Austria have already publicly stated this, but what about other EU member states? 

The fact that a task force has been created in which data protection agencies from various EU member states are involved implies a decision at the EDPB level. The consistency requirement within GDPR ensures that such decisions will be consistent across all member states. This would mean that Google Analytics is illegal in the EU.

There is a debate going on whether the statements from various DPA's also hold for Google Analytics 4 (the new version of Google Analytics). The short answer is yes, so far the statements apply to every version of Google Analytics. We've written about this more extensively in [this blog](https://www.simpleanalytics.com/blog/is-google-analytics-4-gdpr-compliant). 

## Final Thoughts

Before concluding, it might be worthwhile to summarize what we've seen.

In short:

-   After Austria & France, Italy is the third country to declare Google Analytics illegal
-   It's technically not possible to use Google Analytics in a compliant way
-   There won't be a legal framework very soon that says otherwise
-   The consistency requirement within GDPR ensures consistency across all member states

Also worth mentioning: **Consumers demand privacy**.

The business environment is changing, and you should ask yourself if you want to move with it or stick to old beliefs and practices.

Google is even moving away from its current version of Google Analytics by [sunsetting Universal Analytics](https://blog.simpleanalytics.com/google-to-sunset-universal-analytics-in-2023) in favor of GA4. In a statement, they announced that privacy is one of the main drivers for the switch. Although GA4 is still not privacy-friendly, at least they acknowledge that the world is changing.

There are alternatives to Google Analytics that actually care about the privacy of your users. Simple Analytics is one of them, but before I tell you that we are the best, we've created an in-depth [comparison with other privacy-friendly alternatives](https://blog.simpleanalytics.com/4-privacy-friendly-google-analytics-alternatives) to make your own decision.

We believe it's not only a matter of staying within the law. Yes, that's important too. But it goes beyond that. We believe you can still make decisions based on website data without needing to collect personal data or track individuals.

That's why we built Simple Analytics. To provide you with the insights you need while protecting the privacy of your users and being 100% GDPR compliant. If this resonates with you, feel free to [give us a try](https://simpleanalytics.com/welcome).
