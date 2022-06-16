---
title: "CNIL Update: Google Analytics is (still) illegal"
author_slug: iron
author: Iron Brands
excerpt: "CNIL provided a Q&A on the statement made that Google Analytics violates GDPR"
image: https://assets.simpleanalytics.com/blog/2022-french-data-protection-update-google-analytics-is-still-illegal/social-image.png
draft: true
---

First paragraph

{% include gif.html slug="spy-kids-better-look-closer" alt="Spy Kids: Better look closer" width="300" height="201" color="#594748" %}

<img src="https://assets.simpleanalytics.com/blog/google-alternatives/google-analytics-dashboard.png" alt="Caption of the image" class="border" />
<p class="caption" markdown="1">
  Caption of the image
</p>

Rest of the article

On the 7th of June, CNIL, the French data protection watchdog, [issued a Q&A](https://www.cnil.fr/fr/cookies-et-autres-traceurs/regles/questions-reponses-sur-les-mises-en-demeure-de-la-cnil-concernant-lutilisation-de-google-analytics) on the use of Google Analytics. This follows up on the statements made earlier this year in which CNIL ruled the use of Google Analytics violated GDPR ([here](https://www.cnil.fr/en/use-google-analytics-and-data-transfers-united-states-cnil-orders-website-manageroperator-comply)).

Since then, the EU and U.S. have announced a privacy shield 2.0. You can find these statements [here](https://ec.europa.eu/commission/presscorner/detail/en/STATEMENT_21_1443) (EU) and [here](https://www.whitehouse.gov/briefing-room/speeches-remarks/2022/03/25/remarks-by-president-biden-and-european-commission-president-ursula-von-der-leyen-in-joint-press-statement/) (US). [We've written](https://blog.simpleanalytics.com/eu-us-privacy-shield-2-0-is-again-a-political-show) about the fact that this is not an agreement with legal merit, and CNIL seems to agree.

The Q&A CNIL explicitly mentioned that using Google Analytics still violates GDPR. In addition, it stated that there are no circumstances under which this is not the case.

In the article at hand, we break down the statements made by CNIL during the Q&A session.

{% include gif.html slug="5-year-old" alt="5 year old" width="480" height="400" color="#574840" %}


1.  Schrems II and the violation of Privacy Shield 1.0
2.  Privacy Shield 2.0 update
3.  Conclusions from Q&A session CNIL
4.  Solutions

Let's dig in!

## 1.  Schrems II and the violation of Privacy Shield 1.0

The current situation with Google Analytics has been kicked off by the [Schrems II ruling](https://www.gdprsummary.com/schrems-ii/) that invalidated the privacy shield 1.0. According to the GDPR, data transfers outside the EU are possible only if adequate safeguards can be used. The privacy shield acted as a mechanism to safeguard these data transfers.

Schrems II invalidated the privacy shield: In short, the EU demands privacy rights for its citizens, which are not adhered to by the U.S. government. By law, Google qualifies as an "electronic communication service provider," meaning that it must disclose data on EU citizens if the U.S. intelligence service asks for it.

As a response, the DSB (Austrian data protection watchdog) and CNIL stated that the [use of Google Analytics violates GDPR](https://blog.simpleanalytics.com/france-rules-google-analytics-to-be-in-conflict-with-gdpr-ruling) and that EU businesses that continue to use Google Analytics can be fined.

## 2.  Privacy Shield 2.0 update

Since then, the U.S and the EU have announced a political agreement that would replace the invalidated privacy shield. We've written about it [here](https://blog.simpleanalytics.com/eu-us-privacy-shield-2-0-is-again-a-political-show) and touched upon the fact that the deal has no legal merit. It was instead a political agreement. There is still no legal document, which will take a while to finalize.

This was also noted by CNIL during their Q&A session last week. They specifically mentioned that the joint statement is not a legal framework and cannot be relied upon. CNIL expects it may not happen until the end of the year until a deal is finalized. However, when it's finalized, it will almost certainly face fresh legal challenges to see whether it is indeed not just as flawed as Privacy Shield 1.0. To give some perspective, Privacy Shield 1.0 was declared invalid in July 2020. It took until February 2022 for the DSB & CNIL to take proactive enforcement.

<img src="https://assets.simpleanalytics.com/blog/2022-french-data-protection-update-google-analytics-is-still-illegal/handcuffs-no-text.png" alt="CNIL Google Analytics update" class="border" />
<p class="caption" markdown="1">
</p>

## 3.  Conclusion form CNIL Q&A session

According to the French data protection agency, the main conclusion from the Q&A session is that Google Analytics is still illegal. CNIL also confirmed to have issued formal notices to organizations between the first announcement in February and now. Businesses have one month to comply; otherwise, they will receive a fine.

CNIL specifically claims that EU websites should make changes to their use of Google Analytics. However, they also stated that, with the information at hand, the use of Google Analytics is under no circumstances legal. Google proposed different solutions to address this. These were all thrown out of the window by CNIL.

Google confirmed that the data is hosted on U.S. soil, and no change in the eyes of CNIL would prevent the data transfer of personal data. Google proposed two solutions:

-   The anonymization of personal data. 
-   The use of unique identifiers

CNIL discarded both as Google could not demonstrate that data anonymization happened before data transfer to the U.S. The use of unique identifiers was also insufficient as the unique identifiers could be combined with other data.

In addition, CNIL notes that Google is offering more solutions that track IP addresses, meaning these services allow IP addresses to be cross-checked and thus trace the users' browsing history. They also addressed that data encryption won't be sufficient as long a Google has the encryption keys, allowing them to access personal data if they want to.

From the above, we can assume that fines will likely be stepping up. The fact that there are no circumstances under which Google Analytics can be used legally makes for straightforward guidelines. Therefore, enforcement of the ruling has never been easier. 

## 4.  Solutions

The first proposed solution was data encryption, where the key to decrypt the data should be in the hands of the data exporter (or a trusted third party based in the EU). This way, the data of EU citizens are protected from being handed to the U.S. intelligence service.

Another alternative would be the use of a proxy server. This way, there is no direct contact between the data exporter and Google, as the proxy server would act as an intermediary.

The last proposed option would be to ask for explicit consent from users for data transfers. However, this is not a viable fix as it would be a horror to request this to every visitor on every visit. So this might only work under exceptional circumstances.

However, implementing the above solutions might be costly, and the question arises whether these will also meet the operational needs.

If all of this seems subpar to you and you don't want to deal with GDPR hassle anymore, there are privacy-friendly alternatives to Google Analytics. [Simple Analytics](https://simpleanalytics.com/) is one of them. Before shamelessly plugging our solutions as the best solution, we've reviewed all the [privacy-friendly alternatives](https://blog.simpleanalytics.com/4-privacy-friendly-google-analytics-alternatives) and found four solutions you might want to check out.

## Why do we care?

We are an independent team of two that care about privacy and believe the future of web analytics is [cookieless by design](https://blog.simpleanalytics.com/website-analytics-without-cookies). If you are ready to ditch Google Analytics and want to check out what we've built, feel free to [give us a try](https://simpleanalytics.com/welcome).
