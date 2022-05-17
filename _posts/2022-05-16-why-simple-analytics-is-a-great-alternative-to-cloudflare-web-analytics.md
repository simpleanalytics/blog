---
title: Why Simple Analytics is a great alternative to Cloudflare Web Analytics
author_slug: iron
author: Iron Brands
excerpt: What are the differences between Simple Analytics and Cloudflare Web Analytics, and why Simple Analytics is a great alternative.
image: https://assets.simpleanalytics.com/images/blog/why-simple-analytics-is-a-great-alternative-to-cloudflare-analytics/social-image.png
---

A couple of weeks ago, we published our blog post on the four [best privacy-friendly alternatives to Google Analytics](https://blog.simpleanalytics.com/4-privacy-friendly-google-analytics-alternatives). We did not include Cloudflare Web Analytics as one of those, as we believe it's short on a few criteria, and we'll show you why in this article.

{% include gif.html slug="attention-please" alt="attention please" width="480" height="270" color="#38271e" %}

Cloudflare already has an analytics product called Cloudflare Analytics. However, this is a premium product only available for Cloudflare users. The new Cloudflare Web Analytics is free and available for everyone.

Cloudflare Analytics relies on server-side tracking. Cloudflare Web Analytics relies on client-side tracking (like Simple Analytics & Google Analytics).

Server-side tracking involves sending data to a web server before transferring it to third parties. It makes sure that there is more control over the data transfer. In addition, you don't have to worry about ad-blockers or core web vitals because you don't need to add a script to your website. There are drawbacks to server-side tracking as well. Pageviews are highly inaccurate because it's difficult to filter out robots and other automated traffic to your website.

<img src="https://assets.simpleanalytics.com/images/blog/why-simple-analytics-is-a-great-alternative-to-cloudflare-analytics/cloudflare-web-analytics-dashboard.png" alt="Cloudflare Web Analytics Dashboard" class="border-radius" />
<p class="caption" markdown="1">
  Cloudflare Web Analytics Dashboard
</p>

This comparison article will focus on Cloudflare Web Analytics. We'll compare it to [Simple Analytics](https://simpleanalytics.com/) on the following criteria:

1.  [Data insights](#1-data-insights)
    1.  [Sample size data](#11-sample-size-data)
    1.  [Data retention](#12-data-retention)
    1.  [Bot Traffic is not excluded](#13-bot-traffic-is-not-excluded)
    1.  [Differences in features](#14-differences-in-features)
1.  [Privacy](#2-privacy)
1.  [Data interoperability](#3-data-interoperability)
1.  [Ease of use](#4-ease-of-use)
1.  [Pricing](#5-pricing)

## 1. Data insights

The first and foremost difference between Cloudflare Web Analytics and Simple Analytics is the insights both tools provide. There is a stark difference in how both tools collect data and display features. 

### 1.1 Sample size data

Cloudflare Web Analytics does not measure the total traffic to your website. But instead, a small subset of your data is analyzed and measured. This sample is then used to estimate the overall results.

More web analytics tools use data sampling at a certain point. Even Google Analytics uses data sampling whenever your website hits 500,000 monthly page views (in the free version).

The extent to how inaccurate the data is depends on the sample size. In Google Analytics, you can adjust the sample size based on your preferences. You can indicate 'faster results' or 'greater precision' to modify the results. Cloudflare only analyses 1-10% of the traffic coming to your website, which is a very small sample size. You can't adjust the sample size estimates of your real data.

The main reason for data sampling is that it's cheaper. Especially for supposedly 'free' products like Google Analytics and Cloudflare Web Analytics, it makes sense to start working with data samples after a certain point, as costs will outweigh the benefits.

At Simple Analytics, we never sample your data and always show you the actual traffic coming to your website. We believe in giving you the most accurate data while preserving the privacy of your users. 

### 1.2 Data retention

Cloudflare Web Analytics only collects and stores data for six months. Previously this was only seven days. We believe this also has to do with the costs of maintaining servers. Cloudflare Web Analytics is a free product, but servers and maintenance can become expensive. As this is not their core product, we expect that they want to keep the costs down.

However, this is a severe drawback. Most organizations want to measure their analytics over longer periods to see which direction their traffic is heading on specific pages.

At Simple Analytics, we store your data indefinitely (or for as long as you want). It is possible to measure your page views over yearly periods. There is no cap.

<img src="https://assets.simpleanalytics.com/images/blog/why-simple-analytics-is-a-great-alternative-to-cloudflare-analytics/cloudflare-inline-image.png" alt="Simple Analytics vs. Cloudflare Web Analytics" class="border-radius" />
<p class="caption" markdown="1">
  Cloudflare Web Analytics vs. Simple Analytics
</p>

### 1.3 Bot traffic is not excluded

The actual traffic in Cloudflare Web Analytics is inaccurate. This is because they don't exclude bot traffic in their website statistics. Bots are classified as 'Unknown' browser types and are a significant percentage in Cloudflare's website statistics. At Simple Analytics, we exclude bots in your statistics as they do not represent actual page views (we also don't account for bots pageviews in our pricing).

### 1.4 Differences in features

**The number of websites is capped**

There is also a maximum of 10 websites you can add to one account. Again we assume this has something to do with the costs associated with storing data. At Simple Analytics, there is no hard limit to how many websites you can add, but we have a fair use policy. 

**No visit duration**

Cloudflare does not show us the average time-on-page metric. The time-on-page is an essential metric to track how long website visitors stay on your website. We've created our [own time on page](https://blog.simpleanalytics.com/you-are-getting-fooled-by-google-analytics-time-on-page-metric), different from our competitors but more accurate.

**No UTM tags**

Cloudflare does not support UTM tags. Their documentation states that they will likely add it in the future. With Simple Analytics, you can [add UTM tags](https://docs.simpleanalytics.com/how-to-use-url-parameters) to segment referrers.

**No Event Tracking**

Event tracking is also not possible. We are all for straightforward web analytics and honestly believe that 95% of Google Analytics is unnecessary, but event tracking should be in every analytics tool.In an analytics tool that focuses on privacy, you can [still track events](https://docs.simpleanalytics.com/events) based on counts of clicks. Simple Analytics does not use cookies and can record events. For example, for clicks or outbound links. So website owners still get an idea of sign-ups or form downloads based on aggregate data. Not adding event tracking is a huge drawback (although they say they will support it in the future).

**No live visitors**

It's not possible to see live visitors on your dashboard. There is no live version of the product. Check out our [live dashboard](https://simpleanalytics.com/simpleanalytics.com).

**No mini-websites**

Well, we don't want to blame Cloudflare for not adding [mini-websites](https://docs.simpleanalytics.com/mini-websites). Simple Analytics is probably the only tool that transforms boring traffic-referrer links into a mini-website.

<img src="https://docs.simpleanalytics.com/images/mini-websites-simple-analytics.gif" alt="Mini websites as referrers in Simple Analytics vs. Cloudflare Web Analytics" class="border" />
<p class="caption" markdown="1">
  Mini websites in Simple Analytics
</p>

## 2. Privacy
  
Cloudflare claims to be a privacy-friendly analytics tool that does not use cookies or collect personal information and complies with [GDPR](https://gdpr.eu/), [CCPA ](https://oag.ca.gov/privacy/ccpa)& [PECR](https://ico.org.uk/for-organisations/guide-to-pecr/what-are-pecr/). In addition, they state that you don't have to sacrifice privacy to get essential and accurate metrics on the usage of your website. At Simple Analytics, we fully agree with this statement. Privacy is the main reason we started Simple Analytics in the first place. We [never collect any personal data](https://docs.simpleanalytics.com/what-we-collect), not even IP hashes.

Cloudflare Web Analytics seems to be doing a good job from a privacy standpoint. They do not use cookies and also do not collect IP hashes. However, in their [privacy policy](https://www.cloudflare.com/en-gb/privacypolicy/), Cloudflare says that it may collect and process personal information of so-called 'end-users.' It's unclear what they exactly mean by this. Still, you should take note of this when considering Cloudflare Web Analytics. 

## 3. Data interoperability

At Simple Analytics, your data is yours, and we want to make sure you can use it the way you want. Therefore [we offer many APIs](https://docs.simpleanalytics.com/api), including raw level data that can be connected to your dashboarding tools. If you have used Google Analytics before, we allow you to import that data.

Cloudflare provides limited data to be exported to your dashboarding tools. There is an API to export limited data, but importing your Google Analytics data is impossible. In addition, there is zero documentation on connections with dashboarding tools such as Power BI or Google Data Studio.

## 4. Ease of use

For Cloudflare users, it's easy to use Cloudflare Web Analytics because you don't need to add another script to your website. In addition, Cloudflare Web Analytics does not impact your page load speech as much. The script is 4,3kb, whereas Simple Analytics is at 3kb. Google Analytics and Matomo, however, are way bigger and have way more impact on your core web vitals.

One of the main pillars of Simple Analytics is to create a script that does not impact user experience. To see the impact of scripts on page load times, we [conducted a test comparing page load times](https://blog.simpleanalytics.com/google-penalizes-you-for-using-google-analytics) after installing Simple Analytics and Google Analytics. The outcome showed a difference of 10 basis points in favor of Simple Analytics.

## 5. Pricing

> "If you are not paying, you are the product" - Everyone

Just like Google Analytics, Cloudflare Web Analytics is free. We always get suspicious when a service we use is free. Everyone knows the mantra: If you're not paying for the product, you are the product. Everyone knows this because it's true 100% of the time.

Google Analytics is free because Google monetizes the data on your website. As a privacy-friendly web analytics tool, I highly doubt Cloudflare does this. However, it surely costs money to run the service, so what's the strategy here?

It might be a form of 'engineering marketing,' which means they've built a free service to attract users to their main offerings. We shouldn't forget that Cloudflare is a massive company with almost infinite resources. Making a web analytics service to attract more awareness to their other products could be a marketing strategy. If this strategy is not successful, will they keep continuing the product?

Another take is that Cloudflare wants more information concerning page-loading data. Cloudflare's primary offering focuses on deploying websites as soon as possible....

One can only guess what the actual strategy is, but if you are looking for a privacy-first web analytics tool built by a small but dedicated team that fully focuses on analytics, you might want to [give us a try](https://simpleanalytics.com/welcome).

{% include gif.html slug="thumbs-up-iron-adriaan" alt="thumbs up iron adriaan" width="580" height="326" color="#ff4f64" %}
