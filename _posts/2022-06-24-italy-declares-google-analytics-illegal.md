---
title: "Italy declares Google Analytics illegal"
author_slug: iron
author: Iron Brands
excerpt: "The Italian data protection authority declared the use of Google Analytics in violation with GDPR law"
image: https://assets.simpleanalytics.com/blog/2022-italy-bans-google-analytics/social-media.png
draft: true
---

Italy has become the third country to ban Google Analytics officially. The news broke today after a careful examination concluded that Google Analytics violated GDPR law. You can find the statement [here](https://www.gpdp.it/web/guest/home/docweb/-/docweb-display/docweb/9782874#english).

See a copy of the text below...

This news only comes a week after CNIL (French Data Protection Agency) [published guidelines](https://blog.simpleanalytics.com/cnil-update-google-analytics-is-still-illegal) on the Google Analytics matter. These guidelines resulted from the statements made earlier this year in which [CNIL banned the use of Google Analytics](https://blog.simpleanalytics.com/france-rules-google-analytics-to-be-in-conflict-with-gdpr-ruling).

It seems that more and more E.U. states are coming to the same conclusion: Google Analytics is illegal.

{% include gif.html slug="oh-my-god" alt="oh my god" width="480" height="400" color="695957" %}

1.  Italy bans Google Analytics
2.  CNIL Q&A guidelines on Google Analytics
3.  Privacy Shield 2.0
4.  What does the future hold?

Let's dive in!

## 1.  Italy bans Google Analytics

Italy is the third country to ban Google Analytics. This was concluded by Garante (the Italian Data Protection Authority) after a complex investigation in coordination with other European privacy authorities.

It reached the same conclusion as the DSB (Austrian Data Protection Authority), which was the first to rule the use of Google Analytics illegal. This has been the starting point for a chain reaction that led the French and now Italians to follow, and we'll see more in the coming months.

The problem here is the transfer of personal data to the United States. Google is a U.S. company that qualifies as an "electronic communication service provider." This means that Google is by law obliged to disclose data to U.S. intelligence services if requested.

The main reason for introducing the GDPR law in 2018 is to safeguard the privacy of E.U. citizens. The fact that Google transfers data to the U.S. and is obliged to hand it over upon request means the E.U. can no longer guarantee its citizens' privacy.

In declaring that the processing was unlawful, Garante stated that IP addresses were processed by Google and thus consisted of transferring personal data. Even if it were truncated, it would not become anonymous data, given Google's ability to enrich it with other data in its possession.

This is a very important nuance. It means that even if you anonymize IP addresses (like GA4 or Matomo), it's still considered personal data.

## 2.  The French CNIL Q&A Guidelines on Google Analytics

In their Q&A last week, CNIL addressed all the questions raised after they announced Google Analytics to be illegal in February of this year. Since then, Google has suggested different approaches to making sure Google Analytics can be used safely within the E.U. law. However, CNIL concluded that it is technically impossible to use Google Analytics compliantly.

Google has suggested different solutions that were shut down immediately by CNIL:

-   Anonymizing data is not a valid solution because Google could not demonstrate that it does this before transferring the data to the U.S.
-   Data encryption is invalid because if Google still holds the keys, they still have access.

CNIL also stated that a legal agreement between the E.U. & the U.S. is far from established.

## 3.  Privacy Shield 2.0

All of this has been kicked off by [Schrems II](https://iapp.org/news/a/the-schrems-ii-decision-eu-us-data-transfers-in-question/), which invalidated the privacy shield. The privacy shield meant that data transfers outside the E.U. were only possible if adequate safeguards were in place.

Schrems II invalidated this and made it painfully clear that these safeguards for data transfer to the U.S. were not in place. It took a while (1,5 years) for the first E.U. member states to take action to protect the privacy of their citizens. First the Austrian DSB, then the French CNIL, and now the Italian Garante.

After the DSB & CNIL declared the use of Google Analytics illegal, The E.U. and U.S. announced an agreement on a new framework for transatlantic data flow, known as the [Privacy Shield 2.0.](https://blog.simpleanalytics.com/eu-us-privacy-shield-2-0-is-again-a-political-show) However, it became apparent quickly that this agreement had zero legal merits. The announcement was meant as an 'agreement in principle.' It might take very long before a legal document is signed.

## 4.  What does the future hold?

Before concluding, it might be worthwhile to summarize what we've seen.

In short:

-   After Austria & France, Italy is the third country to declare Google Analytics illegal
-   It's technically not possible to use Google Analytics in a compliant way
-   There won't be a legal framework very soon that says otherwise

Not an exact point, but worth mentioning: **Consumers demand privacy**.

The business environment is changing, and you should ask yourself if you want to move with it or stick to old beliefs and practices.

Google is even moving away from Google Analytics by [sunsetting Universal Analytics](https://blog.simpleanalytics.com/google-to-sunset-universal-analytics-in-2023) in favor of GA4. In a statement, they announced that privacy is one of the main drivers for the switch. Although GA4 is still not privacy-friendly, at least they acknowledge that the world is changing.

There are alternatives to Google Analytics that actually care about the privacy of your users. Simple Analytics is one of them, but before I tell you that we are the best, we've created an in-depth [comparison with other privacy-friendly alternatives](https://blog.simpleanalytics.com/4-privacy-friendly-google-analytics-alternatives) to make your own decision.

We believe it's not only a matter of staying within the law. Yes, that's important too. But it goes beyond that. We believe you can still make decisions based on website data without needing to collect personal data or track individuals.

That's why we built Simple Analytics. To provide you with the insights you need while protecting the privacy of your users and being 100% GDPR compliant. If you believe the world is changing and you want to move with it, you might want to [give us a try](https://simpleanalytics.com/welcome).
