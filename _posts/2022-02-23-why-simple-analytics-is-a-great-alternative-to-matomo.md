---
title: Why Simple Analytics is a great alternative to Matomo
author_slug: iron
author: Iron Brands
excerpt: "What are the differences between Simple Analytics and Matomo, and why is Simple Analytics a great alternative."
image: https://assets.simpleanalytics.com/blog/matomo/matomo-versus-simple-analytics.png
lang: en
---

A few weeks back, we published an extensive piece on [the differences between Google Analytics and Simple Analytics](https://blog.simpleanalytics.com/why-simple-analytics-is-a-great-alternative-to-google-analytics). In contrast to Simple Analytics, [Google Analytics](https://analytics.google.com/) is on the complete other end of the spectrum regarding privacy, usability, and extensiveness. However, these tools are taking the middle ground between those far ends.

[Matomo](https://matomo.org/) (formerly known as Piwik) was founded in 2007 as an alternative to Google Analytics. It started as an open-source alternative, and in 2012 the core team joined a team of developers to work on a paid version (now known as Piwik Pro). In 2018, the two teams separated again, and the free version was rebranded to Matomo. So Piwik Pro and Matomo are now two separate companies, with different teams working on both.

This article outlines the key differences between two Google Analytics alternatives: Matomo and Simple Analytics (we will cover PiwikPro later). Both Matomo and Simple Analytics share more similarities with each other than with Google Analytics. Still, there are essential differences worth noting.

Simple Analytics was founded in 2018, and we're still a new kid on the privacy-analytics block. So what are the key differences, and why should you consider Simple Analytics as a Matomo alternative?

{% include gif.html slug="what-is-the-difference" alt="In the end, what is the difference" width="480" height="267" color="#402d2f" %}

### Let's find out!

First of all, we should address the fact that in comparison to Google, Matomo is definitely doing something right. They were the first to challenge Google Analytics back in 2007, and they continue to do so. Matomo has paved the way for companies like us to take on Google, specifically Google Analytics.

However, we started Simple Analytics back in 2018 because we felt there was still much room for improvement. In the next part, we compare Simple Analytics to Matomo in a few key areas which we believe to be very important to provide the best experience: Privacy Friendliness & Compliance, User Interface & Ease of Use, Lightweight vs. Heavyweight script, Data interoperability, Pricing, and lastly, Team.

## Simple Analytics vs. Matomo: What are the key differences

1.  [Privacy Friendliness & Compliance](#1-privacy-friendliness--compliance)
2.  [User Interface & Ease of Use](#2-user-interface--ease-of-use)
3.  [Lightweight vs Heavyweight](#3-lightweight-script-optimized-for-page-speed)
4.  [Data interoperability](#4-data-interoperability)
5.  [Pricing](#5-pricing)
6.  [Team: Two-man army vs Large organization](#6-team-two-man-army-vs-larger-organization)

We've said this before, but we'll do it again: What's the best tool for you, depends on your needs.

In this article, we hope to provide a better understanding of the differences between the two. We make a case for Simple Analytics, but don't just take us up on our words, [give it a try as well and see for yourself](https://simpleanalytics.com/welcome).

## 1\. Privacy Friendliness & Compliance

For us, the most crucial pillar of our product is being compliant with privacy regulations. This is the main reason why we started building Simple Analytics. With regards to Google Analytics and other alternatives, we consider ourselves the only tool to be privacy-first. [We never collect personally identifiable information (PII)](https://docs.simpleanalytics.com/what-we-collect) in any way, not even in a hashed way. Storing anything remotely related to (PII) is a big no-no.

Matomo is considered to be a privacy-friendly alternative to Google Analytics as well. However, it tracks far more data points than Simple Analytics, and in order to do this, it collects personal data. Metrics like bounce rate or session recordings require visitors to be tracked. By default, Matomo is using cookies and is not compliant with [GDPR](https://gdpr-info.eu/) or [GRI regulations](https://www.globalreporting.org/). However, it is possible to make Matomo more privacy-friendly. By taking the following steps, you make Matomo (semi)-compliant with privacy regulations.

1.  Anonymize visitors' IP addresses
2.  Disable cookies
3.  Anonymize URLs that include personal identifiers
4.  Anonymize the tracking data, which includes the user ID and order ID
5.  Anonymize location data, so a full IP address is not used to geolocate visitors
6.  Anonymize all keystrokes which users enter into forms of your site

I'm purposely using the word 'semi' in the text above. Anonymizing data is better than collecting non anonymized data. However, it is still not compliant.

On the 13th of January 2022, the Austrian ([DPA](https://www.data-protection-authority.gv.at/)) watchdog found the use of Google Analytics to be illegal. ([See our article](https://blog.simpleanalytics.com/will-google-analytics-be-banned-in-the-eu) on that one as well for more in-depth information.)

In [their statement](https://noyb.eu/en/austrian-dsb-eu-us-data-transfers-google-analytics-illegal), the DPA addressed the anonymization or collection of 'hashed IP addresses. They called the anonymization of personal data a "technical wrinkle." Basically saying, instead of providing the personal data directly, you turn it into a puzzle, which is still not compliant with European privacy regulations.

In comparison, Simple Analytics is compliant out-of-box. You don't ever need to display annoying cookie banners on your website. We don't make any concessions regarding the privacy of your visitors, and by default, you are fully compliant when using Simple Analytics. The trade-off is that we don't offer features which require users to be tracked, such as session tracking.

If you break it down, it just comes down to this:

Matomo: _"We collect all sorts of data, and the data is yours"_\
Simple Analytics: _"We only collect privacy-insensitive data, and the data is yours"_

## 2\. User Interface & Ease of Use

In terms of the user interface, Matomo is more similar to Google Analytics than to Simple Analytics. In the comparison below, you can see that Simple Analytics is a one-page dashboard with all the relevant website tracking statistics. In contrast, Matomo is more like a full-blown version of Google Analytics.

<img loading="lazy" class="border-radius" src="https://assets.simpleanalytics.com/blog/matomo/matomo-versus-simple-analytics.png" alt="Matomo versus Simple Analytics, the alternative to Google Analytics">
<p class="caption">The interface of Matomo versus Simple Analytics.</p>

At Simple Analytics, we try to stay simple. We provide a one-page dashboard with important metrics like page views, unique visitors & time-on-page. In addition, you get an overview of the geographical spread of your website visitors and what device they use to visit your website. It is also possible to collect events and goal conversion.

Matomo is more extensive than Simple Analytics. It has a Google Analytics feel with multiple charts, many features, and reports. Matomo displays hundreds of different website metrics, and while some might be relevant for a few die-hard marketers, most will not be looked at.

In terms of usability, Matomo might be a bit confusing. One of our customers who switched from Matomo told us that:

"You do need to roll up your sleeves to install Matomo properly, they guide you through the process but you will need some experience to complete it, and trouble-shoot"

After installation, by default, you are not compliant to privacy laws and need to display a cookie banner on your website or go through the steps, as noted earlier in this article, to make your website more privacy-friendly.

## 3\. Lightweight script optimized for page speed

It's an understatement that page speed is important. Adding heavy scripts to your website increases the page load time. In that sense, every KB matters. The script on which we run Simple Analytics is 3kb, seven times smaller than Matomo's (22kb) script.

To see the impact of scripts on page load times, we [conducted a test comparing page load times](https://blog.simpleanalytics.com/google-penalizes-you-for-using-google-analytics) after installing Simple Analytics and Google Analytics (45kb). The outcome showed a difference of 10 basis points in favor of Simple Analytics.

<img loading="lazy" class="border-radius" src="https://assets.simpleanalytics.com/images/blog/lighthouse-compare-share-image.png" alt="Google Analytics compared to Simple Analytics">
<p class="caption">Comparison between using no analytics, Simple Analytics, and Google Analytics.</p>

We didn't perform the test with Matomo, but we are confident that the page speed will be impacted as the script Matomo is using is seven times bigger.

## 4\. Data Interoperability

Simple Analytics has maybe ways to get your data out. For example, you might want to move your data to a data lake (like [Snowflake](https://www.snowflake.com/)) or build your own reports. [We offer many APIs](https://docs.simpleanalytics.com/api), including raw level data, which means that every row in the export is one page view.

If you have used Google Analytics before, we allow you to import that data. We believe the data is yours, and you should be able to use it your way. Matomo [does offer a way](https://matomo.org/docs/google-analytics-importer/) to import Universal Google Analytics properties (no sign of GA4 properties yet). It's a very long and complex tutorial, so if you're brave, it's fine. If you want to be done in a few clicks, check out the importer of Simple Analytics.

Matomo and Simple Analytics both have no [data sampling](https://matomo.org/no-data-sampling/). This is better for more accurate numbers, unlike Google Analytics.

## 5\. Pricing

Matomo provides two options: Self-hosted and cloud-hosted.

Self-hosted is the free version of their product (although you need to pay for your servers and need to have quite a lot of technical expertise). In addition, if you want to add more features, you need to pay extra.

The cloud-hosted version is similar to what Simple Analytics offers. Both companies charge based on the number of 'hits' or website visits. By comparing both cloud-hosted solutions, we can see quite a stark difference in pricing:

| | 100k visits | 1 Million visits |
| Simple Analytics | 19 Euros | 59 Euros |
|Matomo|35 Euros|159 Euros|

For websites with around 100k visits, Matomo is twice as expensive and for bigger websites, it's almost three times as expensive.

We have to note that Matomo provides more reports, charts, and metrics to track than Simple Analytics. Their product has more features. For some, this is preferred over a simpler solution like Simple Analytics, but it also has its drawbacks.

First of all, this makes the product more expensive and less privacy-friendly. Using heatmaps is a feature provided by Matomo, which is not compliant at all. In addition, having more features decreases your website speed and can make it less intuitive to use.

## 6\. Team: Two-man army vs. larger organization

At Simple Analytics, next to being privacy-first, providing the best experience for our users is our top priority. We know we are tiny fish in a pond that a few whales dominate. Therefore, we appreciate users who have faith in our small team and product. We've created an open roadmap for our users to view and interact with to show this. Our users have a say in which direction we are heading. In addition, you can reach us 24/7 through our telegram chatbox, mail, Twitter. The founder himself will handle your questions, and we will try to answer them as quickly as possible. The only way to get in touch with the Matomo team is through email.

Matomo is one of the largest web analytics tools out there. At least [1% of all the websites ](https://w3techs.com/technologies/details/ta-matomo)on the internet are using Matomo. It's a great success, and it paved the way for independent projects like Simple Analytics to take on Google.

Choosing to work with Simple Analytics, you decide to work with an independent project and support a two-man team striving for a privacy-friendly web. Find out for yourself and [give us a try](https://simpleanalytics.com/welcome).
