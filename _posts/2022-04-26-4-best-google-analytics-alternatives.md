---
title: 4 Best Google Analytics Alternatives
author_slug: iron
author: Iron Brands
excerpt: "There are more and more privacy-friendly Google Analtyics alternatives, but which one is the best?"
image: https://assets.simpleanalytics.com/blog/google-alternatives/spectrum-privacy-friendly-analytics.png
draft: true
---

The call for privacy-friendly Google Analtyics alternatives has never been this high. More and more businesses are turning their back on Google Analytics after the French and Austrian 'Data Watchdogs' considered it is [violating privacy regulations.](https://noyb.eu/en/austrian-dsb-eu-us-data-transfers-google-analytics-illegal)

But what is the best alternative to Google Analytics? With more and more options entering the market, it might be hard to distinguish these alternatives from one another. That's why we decided to do some research.

We've already written an [in-depth comparison focusing on the privacy part](https://blog.simpleanalytics.com/4-privacy-friendly-google-analytics-alternatives). However, privacy is only one part of the equation (albeit the most important one). This article focuses on the other parts: **Data insights, ease of use, data interoperability, and costs.**

Consider this part 2.

{% include gif.html slug="bring-it-on" alt="bring it on" width="480" height="400" color="#6c6362" %}

In this article we'll be benchmarking the privacy-friendly Google Analytics alternatives on the following properties:

-   Data Insights: What insights do they provide? 
-   Ease of use: How easy is it to get started?
-   Data Interoperability: How easily does it work with other tools?
-   Costs: How expensive is it to use?

Let's dive in!

## Google Analytics Alternatives

Google Analytics is the default web analytics tool for the majority of the internet. 80% of the websites using an analytics tool are using Google Analytics. It's a free and very powerful tool that tracks every move of every website visitor.

Google Analytics is the number one in the web analytics market regarding data insights, but it faces many issues concerning privacy and ease of use. Therefore, the market for Google Analytics alternatives is growing. 

Like our last comparison article, we'll compare the same four alternatives we believe are worth looking into:
- [Simple Analytics](https://simpleanalytics.com/)
- [Plausible](https://plausible.io/)
- [Matomo](https://matomo.org/)
- [Fathom](https://usefathom.com/)

Full disclosure: This article is written by Simple Analytics. Yes, we might be biased, but we try our best to benchmark Simple Analytics as independently as possible.

## 1. Simple Analytics

<img src="https://assets.simpleanalytics.com/blog/google-alternatives/simpleanalytics-dashboard-top.png" alt="simpleanalytics dashboard" class="border" />
<p class="caption" markdown="1">
  Simple Analytics dashboard
</p>

Simple Analytics is the furthest away from Google Analytics in many ways. This is because Simple Analytics [never collects any personal data or uses cookies.](https://blog.simpleanalytics.com/website-analytics-without-cookies) As mentioned earlier, this does impact the depth of data insights.
  
### Data Insights
Collecting sessions over multiple days is not possible with Simple Analytics. It is still possible to differentiate page views and [unique visitors based on the referrer domain.](https://docs.simpleanalytics.com/explained/unique-visits) This is less accurate than tracking sessions but more privacy-friendly. However, the page views reported by Simple Analytics are more accurate than Google Analytics because you don’t need cookie consent using Simple Analytics. Unlike Google Analytics, Simple Analytics bypasses adblockers by default.

It is also possible to use UTM codes to see which specific sources generate traffic to your website, and you can track events. We've set up an automated events script that collects downloads, outbound links, clicks on email links, and you can add your custom events.

### User Experience
Whereas Google Analytics welcomes you with 75 reports and multiple dashboards, Simple Analytics has a [one-page dashboard](https://simpleanalytics.com/simpleanalytics.com) that shows you the most important metrics in a straightforward overview.

Everything is clickable in the overview, so segmenting is easy. Simple Analytics also visualizes source links. For example, clicking on 'Twitter' in the referrer section gives you an overview of Twitter traffic and shows the exact tweets that caused the traffic spike.

{% include video.html slug="2022-04-26-twitter-viewer" %}

In addition, Simple Analytics is a lightweight analytics tool (3kb). Switching from Google Analytics (45kb) will increase your page load speed, increasing your website visitors' user experience.

### Data interoperability
It's possible to import your Google Analytics data directly into Simple Analytics, so you won't lose any historical data by switching to Simple Analytics.
It's also easy to export your data from Simple Analytics using the API. In addition, there are multiple integrations with dashboarding tools like Power Bi and Google Data Studio.

### Costs
Simple Analytics has two plans. The Starter plan and the Business plan.
- Starter Plan: 19$ (or 9$ on a yearly deal) for up to 100,000 page views per month.
- Business plan 59$ (or 49$ on a yearly plan) for up to 1 million page views per month.
- After 1 million pageviews, Simple Analytics offers custom deals.
  
## 2. Plausible

<img src="https://assets.simpleanalytics.com/blog/google-alternatives/plausible-dashboard-top.png" alt="Plausible dashboard" class="border" />
<p class="caption" markdown="1">
 Plausible dashboard
</p>

Plausible is closer to Simple Analytics than Google Analytics and is also built by a small team focused on privacy and ease of use.

### Data Insights
Plausible does use of cookies and only collects personal data anonymized for 24 hours. This approach aligns with their privacy vision and provides more data insights. By collecting hashes of IP addresses for 24 hours, Plausible can track sessions on the same day, making their unique visitor count more accurate. Conversions on the same day can be attributed as well. It's, therefore, easier to set goals and track conversions. In addition, they can show visitors' locations on the city level, whereas Simple Analytics does this on the country level.

In comparison to Simple Analytics, they provide more data but are also less privacy-friendly.

### User Experience
Plausible looks similar to Simple Analytics in that they use a one-page dashboard to show key metrics. It also works the same in that everything is clickable, and segmenting is easy. The UI looks good, and it's built in an intuitive way. 

Plausible is also a lightweight web analytics tool (1kb). The impact on your page load speed is, therefore, very low. Switching from Google Analytics to Plausible will positively affect your page load speed. 

### Data Interoperability
For a few weeks, it's now possible to import data from Google Analytics directly into Plausible. You won't have to deal with a loss of historical data moving to Plausible. It also has an API to export your data. However, this is limited to aggregated data. Simple Analytics offers both raw and aggregated data. This makes it possible to analyze your data yourself on a very deep level. From the docs on their website, we don't see any integrations with dashboarding tools like Power Bi or Google Data Studio.

### Costs
Plausible is open source. If you are technical, you can host your analytics. This means you still need to pay for hosting and make sure to keep the software up to date yourself. Plausible also offers paid solutions:
- 9$ Per month for up to 10,000 pageviews. 
- 19$ Per month for up to 100,000 pageviews 
- 69$ Per month for up to 1 million pageviews

## 3. Matomo

<img src="https://assets.simpleanalytics.com/blog/google-alternatives/matomo-dashboard.png" alt="Matomo dashboard" class="border" />
<p class="caption" markdown="1">
  Matomo Dashboard
</p>
  
Matomo is the oldest alternative to Google Analytics. They teamed up with Piwik Pro in the early days but went on their own again in 2018. Their focus is more on data insights and less on the privacy of the people where this data is collected of.

### Data insights
Where Plausible and Simple Analytics are similar in that they are “simple,” Matomo is more complex. In their default mode, Matomo uses cookies and collects IP addresses (in an anonymized way). Hence you can get more insights than Simple Analytics or Plausible because visitors are tracked individually. 

### User Experience
From the screenshot of their dashboard above, you can see that it needs a lot in common with Google Analytics. Matomo welcomes you with multiple dashboards and reports. It is more complex than the easily segmentable one-page Simple Analytics and Plausible dashboard. In addition, the page load speed is also impacted when installing Matomo on your website. Their script is seven times larger than Simple Analytics’ script (22kb).  

Matomo is a comprehensive tool, but it has many directions and tutorials to understand how it works. For example, it's possible to use Matomo in a cookieless version, but it takes you through many tutorials and custom steps to get started. 

### Data Interoperability
You can import your historical data from Google Analytics in Matomo. However, this is a long and complex tutorial, so if you are brave, you are fine. However, it offers an integration with Google Data studio, not with other dashboarding tools. 

### Costs
Matomo is open source and can be used for free on-premise. If you are technical, you can host your analytics. They also offer a paid version:
- 35$ for up to 100,000 pageviews
- 159$ for up to 1 million pageviews

For an in-depth comparison between Matomo and Simple Analytics, you should check [this article](https://blog.simpleanalytics.com/why-simple-analytics-is-a-great-alternative-to-matomo). 

## 4. Fathom

<img src="https://simpleanalyticsassets.b-cdn.net/blog/google-alternatives/fathom-dashboard-top.png" alt="Fathom dashboard" class="border" />
<p class="caption" markdown="1">
  Fathom dashboard
</p>

Fathom has the philosophy of displaying a straightforward dashboard with all the key metrics and focuses on privacy. It is very similar to Plausible and Simple Analytics in a lesser sense.

### Data insights
Fathom doesn’t install cookies and only collects hashes of IP addresses for 24 hours. They take the same approach as Plausible. Collecting IP hashes provides more data while staying on the good side concerning privacy. However, IP hashes are still considered personal data and might lead to privacy issues in the future. 

### User Experience
Also, in terms of user experience, it's similar to Plausible and Simple Analytics. However, the dashboard seems a bit less intuitive than the other two. It feels less easy to navigate, and the colors make it less clear than Simple Analytics or Plausible. 

The impact on page load speed, however, is also minimal. Switching from Google Analytics to Fathom would positively affect your page load speed. 

### Data Interoperability
From their documentation, we could not find if it was possible to import Google Analytics data into Fathom. However, in their latest blog post, they suggest they are building something that would make this possible.

Through their API, it is already possible to export your data directly into your favorite dashboarding tools. However, similar to plausible, this is limited to aggregated data. Fathom does not offer the possibility to export raw level data. 

### Costs
Fathom is not open source. They only offer a paid solutions:
- 14$ for up to 100,000 pageviews
- 54$ for up to 1 million pageviews

## Conclusion

The conclusion of this piece: There is no single 'best' alternative.

It ultimately depends on your needs in terms of data and your stance toward privacy. There is a privacy trade-off: The more data you want to collect on the individual level, the more privacy-invasive tools you will need. 
  
<img src="https://assets.simpleanalytics.com/blog/google-alternatives/spectrum-privacy-friendly-analytics.png" alt="privacy vs. data insights" class="border" />
<p class="caption" markdown="1">
  The Privacy Trade-off
</p>

You need to decide how important the privacy of your visitors is to you and what data you really need to make decisions.

Data-hungry organizations will be more likely to use either Matomo or Google Analytics, as those two provide the most data. Whereas privacy-conscious organizations that want to see what's happening on their website but don't need to track everyone individually will opt for Simple Analytics, Plausible, or Fathom.

Privacy-friendly solutions are here to stay. Choose the one that fits your needs while preserving the privacy of your users. They will be thankful.
