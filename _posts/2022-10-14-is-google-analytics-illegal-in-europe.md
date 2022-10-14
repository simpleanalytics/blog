---
title: "Is Google Analytics illegal in Europe?"
author_slug: carlo
author: Carlo Cilento
excerpt: "Google Analytics has been declared in violation with GDPR by multiple EU Member States. Is Google Analytics now illegal in Europe?"
image: https://assets.simpleanalytics.com/blog/2022-
image_no_text: https://assets.simpleanalytics.com/blog/2022-
related_posts:
 - /blog/why-its-time-to-move-away-from-google-analytics
 - /blog/why-simple-analytics-is-a-great-alternative-to-google-analytics
 - /blog/how-to-delete-google-analytics-in-4-steps
 - /blog/website-analytics-without-cookies
draft: true
---

First paragraph

{% include gif.html slug="spy-kids-better-look-closer" alt="Spy Kids: Better look closer" width="300" height="201" color="#594748" %}

<img src="https://assets.simpleanalytics.com/blog/google-alternatives/google-analytics-dashboard.png" alt="Caption of the image" class="border-radius" />
<p class="caption" markdown="1">
  Caption of the image
</p>

Google Analytics has been on the front page of the privacy news lately. [Austria](https://gdprhub.eu/index.php?title=DSB_(Austria)_-_2021-0.586.257_(D155.027)), [France](https://gdprhub.eu/index.php?title=CNIL_(France)_-_Google_Analytics_(no_case_number)), [Italy](https://gdprhub.eu/index.php?title=Garante_per_la_protezione_dei_dati_personali_(Italy)_-_9782890), and recently [Denmark](https://www.simpleanalytics.com/blog/denmark-declares-google-analytics-unlawful) have ruled the use of Google Analytics unlawful in its current setup. The rulings are part of a coordinated effort on a European level and have been in the works for a long time.

GA is the default analytics tool, and it's used by [55%](https://w3techs.com/technologies/overview/traffic_analysis) of all the websites on the web. It has long been a monopolist on the web analytics market, and its legal troubles are sending waves across the marketing landscape in Europe. In this climate of general panic, it can be challenging to understand what European authorities are ruling exactly. Is Google Analytics really illegal in Europe?

![](https://lh5.googleusercontent.com/qVJRqySI1XKzVJJpBrfvjGreemm22qmel_0giwdEHi0_95z0HWeprlhJzjVtf5_YAWNXNFb-mDFAppw0cs9ZSnAPCXGDU769ek4HsuLqzoz4fzZ92CZso9QQ3uSMr0lXu6gU9ZgdUrd3utj5aNEvBtp9O-W31Ia0KkyR-0GCJqbu51a5DyqCsD3-Cw)

1.  The background on Google Analytics and GDPR
2.  What did the authorities actually say?
3.  Where is Google Analytics illegal?
4.  Where else will it be illegal?
5.  What about the new data transfer framework?

Let's dive in!

## 1. The background on Google Analytics and GDPR

Google Analytics came under fire because it requires transferring personal data to the U.S. for processing. Data transfers to the U.S. are a legal puzzle right now. It's a long story, and you can read all about it [here](https://www.simpleanalytics.com/blog/how-to-move-forward-with-data-transfers-between-the-eu-us). In a nutshell:

-   The [Schrems II](https://www.google.com/search?q=gdprhub+schrems+II&oq=gdprhub+schr&aqs=chrome.0.69i59j69i57j69i59l2j69i60l2.3865j0j1&sourceid=chrome&ie=UTF-8) ruling of the Court of Justice requires companies to implement adequate safeguards (commonly referred to as supplementary measures) when transferring data to the U.S. to protect data from State surveillance
-   NGO noyb filed [101 complaints](https://noyb.eu/en/101-complaints-eu-us-transfers-filed) against Google Analytics and Facebook Connect to nudge European authorities towards stricter enforcement of the Schrems II ruling.
-   The board of European supervisory authorities (EDPB) [coordinated the response to the complaints](https://edpb.europa.eu/news/news/2020/european-data-protection-board-thirty-seventh-plenary-session-guidelines-controller_en) at a European level.
-   Several European Data Protection Authorities (DPAs) have "banned" GA from the respective countries[1].

## 2. What did the authorities actually say?

The complaints and decisions on Google Analytics are very similar. This is how they all played out so far:

-   A data subject represented by noyb claimed that a website using GA transferred their personal data to the U.S. without effective safeguards
-   The owner of the website protested that the safeguards implemented in the GA Terms of Service were sufficient
-   The DPA examined the safeguards and concluded that they were ineffective against State surveillance
-   The DPA ordered the website to stop using GA (or implement stronger safeguards, which is impossible).

According to the Schrems II case, supplementary measures for data transfers must be evaluated case by case. So a DPA can't declare Google Analytics unlawful per se because, in theory, a different website could implement stronger safeguards and use GA lawfully.

*'Theory'* is the key word here. In practice, the supplementary measures are chosen by Google and accepted by any company agreeing to GA's standard Terms of Service. Because every company agrees to the exact same Terms of Service, **the supplementary measures are always the same**. If a DPA holds that the measures are inadequate in a specific case, it will do the same in future cases because all cases are carbon copies of each other.

But can't a website implement supplementary measures of its own on top of Google's? Unfortunately, it cannot. There are very few effective safeguards against State surveillance, and **none of them can be used for Google Analytics** (we wrote more about this in our [Data Transfers blog](https://www.simpleanalytics.com/blog/how-to-move-forward-with-data-transfers-between-the-eu-us)). A proxy server might be an effective solution, but it severely limits GA's analytical capabilities and is burdensome to implement.

Bottom line: the decisions are about specific websites, but because all websites use the same safeguards, each decision sets a **general precedent that practically amounts to a Statewide ban**.

## 3. Where is Google Analytics illegal?

So far, three DPAs have ruled against GA: the Austrian DSB, the French CNIL, and the Italian GPDP. This means that **Google Analytics is practically banned in Austria, France, and Italy**. It should be noted that the CNIL and the GPDP are quite influential at a European level: if they adopt the approach coordinated by the EDPB task force, other DPAs will likely follow their example.

The Italian situation is peculiar. In a [press release](https://www.garanteprivacy.it/home/docweb/-/docweb-display/docweb/9782874#english) following its first decision against GA, the Italian DPA warned that they would further investigate the use of analytics tools (especially GA) for Italian data controllers, including public administrations. Additionally, the hacktivist group [MonitoraPA](https://monitora-pa.it/) (which translates to monitoring the public administration) emailed thousands of public and private companies by email and requested them to stop using Google Analytics and Google Fonts, threatening legal action before the DPA. MonitoraPA's initiative is somewhat controversial and widely discussed in the Italian privacy community and among marketing professionals.

In practical terms, GA is also **banned in Denmark**. The Danish DPA was not involved in the 101 complaints and didn't settle any case on GA. It examined GA's on its own instead after other DPAs ruled against GA and declared in a recent [press release](https://www.datatilsynet.dk/english/google-analytics/use-of-google-analytics-for-web-analytics) that it cannot be lawfully used unless effective supplementary measures are implemented. The only example they provided was a reference to the CNIL and EDPB's suggestion to set up a **proxy server** in order to anonymize all personal data. This is very complex and prohibitively expensive for most companies.

## 4. Where else will it be illegal?

Noyb's complaints were filed in front of every European DPA. No details are known about the complaints right now, but as we explained, some DPAs will likely follow the example set by Austria, France, and Italy.

Notably, in a January [press release](https://autoriteitpersoonsgegevens.nl/nl/onderwerpen/internet-telefoon-tv-en-post/cookies#hoe-kan-ik-bij-google-analytics-de-privacy-van-mijn-websitebezoekers-beschermen-4898), the **Dutch DPA** announced that it was investigating two controllers for using GA and might rule against GA in 2022. No other details on the cases are available at the moment.

It's worth mentioning that the **Irish DPA**  [drafted a decision](https://iapp.org/news/a/irish-dpc-files-draft-order-to-halt-metas-data-transfers-to-us/) to shut down Meta Platform Ireland's data transfers to Meta in the US. The draft has now been submitted to the EDPB, so the case's outcome is still uncertain. The case does not involve Google, but the fundamental issues with Meta's data transfers are those analyzed by DPAs in noyb's complaints so that it might set an important precedent for other companies, including Google. An Irish precedent would be a big deal because many US tech multinationals have European branches in Ireland.

## 5. What about the new data transfer framework?

In recent news, US President Joe Biden published an [executive order on US surveillance programs.](https://www.whitehouse.gov/briefing-room/presidential-actions/2022/10/07/executive-order-on-enhancing-safeguards-for-united-states-signals-intelligence-activities/) The goal is to curtail US surveillance practices and build a new framework for transferring data.

This is not the first data transfer framework between the US and the EU. There were two older frameworks (Safety Harbor and Privacy Shield), and the CJEU invalidated both in the Schrems I and II rulings over surveillance concerns. The new framework will certainly be challenged in Court, probably by Schrems himself and noyb. This is why the new executive order addresses surveillance practices: the President is trying to fix the issues highlighted in the Schrems II ruling so the new framework can survive Schrems III.

Data controllers will not be able to rely on the new data transfer framework until the European Commission adopts an adequacy decision. This will almost certainly happen, but it's not clear when- it will probably take several months. And crucially, the adequacy decision will need to survive a Schrems III decision afterward, which we are doubtful of. 

## Final Thoughts

It's hard to say right now how Schrems III will play out. The new executive order and the possible outcome of Schrems III will be a hot topic in the privacy community for months to come.

Whether the adequacy decision will survive Schrems III or not, Google Analytics is a privacy-invasive tool. From an ethical standpoint, we believe that Google is not helping to create an independent web that is friendly to website visitors. And why should they? They are raking in billions with Google Analytics.

This is the reason why we built [Simple Analytics](https://www.simpleanalytics.com/). A web analytics tool that provides you the [insights](https://simpleanalytics.com/simpleanalytics.com) you need without any tracking or collecting personal data.

Feel free to[ give us a try](https://simpleanalytics.com/welcome) if you want to support an independent business that is trying to create a web that is friendly to website visitors.

>[1]: The gpdrhub has summaries for the Austrian, French and Italian decisions.
