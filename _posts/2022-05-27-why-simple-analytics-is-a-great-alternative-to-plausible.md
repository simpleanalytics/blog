---
title: "Why Simple Analytics is a great alternative to Plausible"
author_slug: iron
author: Iron Brands
excerpt: "Comparison blog between Simple Analytics and Plausible and why Simple Analytics is a great alternative to Plausible."
image: https://blog.simpleanalytics.com/images/
draft: true
---

The market for analytics tools is scattered. 100+ web analytics companies want to dethrone Google Analytics. Some focus on more tracking and insights, whereas others, like Simple Analytics, focus on less tracking and more privacy. Of all the analytics tools, Plausible is closest to Simple Analytics.

At Simple Analytics, we often get the question of how we are different from Google Analytics, but the real privacy enthusiast asks us how we are different from Plausible. This is way more nuanced as both solutions have a similar approach.

Plausible & Simple Analytics are both:

-   founded by a small team of Indie developers
-   bootstrapped without external funding
-   privacy advocates
-   transparent 
-   simplistic by design

However, there are still differences. In this article, we'll find out what those differences look like.

<img src="https://assets.simpleanalytics.com/blog/why-simple-analytics-is-a-great-alternative-to-plausible/plausible-vs-simple-analytics.jpeg" alt="Simple Analytics vs. Plausible" class="border" />
<p class="caption" markdown="1">
  No they are not
</p>

As we have done in previous comparisons, like the one with Google Analytics, we will look at different aspects.

1.  [Data Insights](#1-data-insights)
2.  [Privacy friendliness](#2-privacy-friendliness)
3.  [Data Operinterability](#3-data-operinterability)
4.  [Ease of use & features](#4-ease-of-use-features)
5.  [Costs](#5-costs)

Let's dive in! 

## 1. Data Insights

The extensiveness of data insights is always interlinked with privacy-friendliness. This means that the more data insights are provided, the less privacy-friendly it usually is.

Google Analytics provides tons of data. It tracks so many data points that 95% is irrelevant. It does this by collecting personal data and installing cookies on your browser. They know where you live and [more](https://spreadprivacy.com/what-does-google-know-about-me/). Google Analytics is the ultimate example of collecting extensive data insights while disregarding privacy in any form.

Simple Analytics and Plausible differ from Google in their approach. Both value privacy over data insights. However, there are varying degrees between them.

Simple Analytics does not collect any personal data or use cookies at all. Therefore, it is impossible to collect session data on an individual user for multiple days. Simple Analytics is built with a privacy-first approach from the ground up. All the metrics in the dashboard are based on non-personal data.

No personal data and being [cookieless by design](https://blog.simpleanalytics.com/website-analytics-without-cookies) does not necessarily mean that all the data is flawed or inaccurate. It is still possible to differentiate page views from unique visitors based on the referrer domain. This method is admittedly less accurate than tracking sessions but more privacy-friendly. However, page views reported by Simple Analytics, for example, are more accurate than page views in Google Analytics with our [adblocker bypass](https://docs.simpleanalytics.com/bypass-ad-blockers).

With Simple Analytics, [you can still use UTM codes](https://docs.simpleanalytics.com/how-to-use-url-parameters) to see which specific sources generate traffic to your website. In addition, event tracking is possible as well. We've set up an [automated events script](https://docs.simpleanalytics.com/automated-events) that collects downloads, outbound links, and clicks on email links, and you can add your custom events.

<img src="https://assets.simpleanalytics.com/blog/google-alternatives/simple-analytics-dashboard.png" alt="Simple Analytics dashboard" class="border" />
<p class="caption" markdown="1">
  Simple Analytics dashboard
</p>

As mentioned above, Plausible takes a similar approach as Simple Analytics. However, the most significant difference is that Plausible collects data differently. They can show all of the Simple Analytics metrics and just a little more.

For example, in addition to event tracking, Plausible shows conversions, and they can provide bounce rates. Simple Analytics shows conversions as well. But they only work within one session. A Simple Analytics session is usually only one page. Except when you have a SPA (single page application). Then the sessions are until the website is closed or refreshed.

Also, the location of your website users can be indicated on the city level by Plausible. In Simple Analytics, this is only possible at the country level. We don't use an IP address to indicate the country. Instead, we use [timezone](https://simpleanalytics.com/timezone).

Plausible can show more data insights than Simple Analytics because they do collect hashes of IP addresses for 24 hours. This means that they 'anonymize' the IP address to track an individual user for a day.

They can attribute conversions on the same to a specific IP hash, providing more insights into which referral sources are converting more than others. This is relevant data but also less privacy-friendly. 

<img src="https://assets.simpleanalytics.com/blog/google-alternatives/plausible-dashboard.png" alt="Plausible dashboard" class="border" />
<p class="caption" markdown="1">
  Plausible dashboard
</p>

Both Plausible and Simple Analytics also use a different approach to Google Analytics. They use timestamp hits to indicate the time on page. We analyzed how Google Analytics calculates time on page and concluded that they are off.

1.  Google Analytics doesn't record the time on page if the visitor only visits one page.
2.  Google Analytics doesn't record the time on page of the last page visited
3.  Google Analytics records time on page if you leave a tab open but are 'spending time' in a different tab.

In addition, Google Analytics includes bounced visitors, but their time on page is set to 10 seconds by default.

Plausible excludes bounced visitors entirely from the calculation, but it uses the method as Google Analytics does. It, therefore, shows a higher than actual number on average time on page.

At Simple, we detect when a visitor navigates to a different website. In comparison to Google Analytics, we record the time on page for a bounced visitor and the time on page for the last visited page. In addition, we've researched the best method to calculate the average time on page. To filter out outliers, we use the median instead of the mean to get to the most accurate number. As a result, the [time on page using our method](https://docs.simpleanalytics.com/explained/time-on-page) is expected to be lower than in Google Analytics.

## 2. Privacy: Privacy-friendly vs. Privacy-first

Without a doubt, Simple Analytics and Plausible are both companies that value privacy and share a common belief in making the internet a safer place. However, the degree varies. This is perfectly illustrated on both homepages.

(insert image regarding both homepages)

Simple Analytics: *Privacy-**first**

Plausible: *Privacy-**friendly**

Plausible also mentions this in their data policy: *"Plausible attempts to strike a reasonable balance between de-duplicating pageviews and staying respectful of visitor privacy."*

Whereas Simple Analytics states that *["We never collect IP addresses or any form of personal data."](https://docs.simpleanalytics.com/what-we-collect)*

### 2.1 Are IP hashes considered personal data?

IP hashing means transforming an IP address into an unrecognizable string of numbers. It's a technique used to track an individual's behavior without directly collecting and storing the IP address.

IP hashing is more privacy-friendly, and Plausible collects the IP hashes for 24 hours. However, at Simple Analytics, we consider this fingerprinting, and we believe this falls under tracking in the GDPR as well, for which you would need consent.

Something can be considered fingerprinting if it is possible to single out a specific visitor by combining information such as pixel density, device identifier, default language, and timezone. A hash of IP basically does the same. It singles out an individual user.

This conflicts with GDPR law.

[Article 4 of the GDPR](https://gdpr-info.eu/art-4-gdpr/) states that personal data relates to any information relating to an identified or identifiable natural person ('data subject'). In addition, different kinds of identifiers are mentioned. It doesn't describe any specific technologies, such as fingerprinting, but one could interpret this from the statement.

This is a grey area, to say the least, and we want to stay away from those. We believe that you can provide actionable data insights without collecting any personal data (even if it's only for 24 hours). It's not our goal to just comply with GDPR law but to protect the privacy of internet users regardless.

## 3. Data interoperability

There are many ways to get your data out of Simple Analytics. We believe this is our duty as the data we collect is yours, and so you should do with it whatever you want. The information Google Analytics collects, for example, is theirs. That's why Google Analytics is free. You pay with your data.

Simple Analytics makes it easy to connect your dashboarding tools. For example, you might want to build your own reports and move your data to a data lake (like Snowflake). [We offer many APIs](https://docs.simpleanalytics.com/api), including raw level data, which means that every row in the export is one page view or event (we call them data points).

It's also very easy to get your data in. Users who want to switch to Simple Analytics can [import Google Analytics data](https://docs.simpleanalytics.com/import-google-analytics-data). You won't have to deal with the loss of historical data.

A lot of the above is also possible in Plausible. They recently added the feature to import Google Analytics data as well. In addition, Plausible also provides different APIs to connect your data with dashboarding tools. However, the APIs are only limited to aggregate data. Simple Analytics offers both aggregated data as well as raw data. We believe raw data is trivial to analyze the data the way you want. When combined with other data sources, you don't really want aggregated data. We see many enterprise customers combining data from different sources into one to get their KPIs.

## 4. User Experience & features

At first hand, Simple Analytics and Plausible look similar. Both have built a one-page dashboard that provides the most valuable website metrics at a glance. Whereas Google Analytics shows you 75 reports when opening the dashboard, Plausible and Simple Analytics stay simple. Everything in the dashboards is clickable, and it's very easy to segment and see which pages are performing better than others.  

### 4.1 Lightweight script

Both Simple Analytics (3kb) and Plausible (>1kb) are lightweight web analytics tools. Google Analytics, for example, uses a script that is 45kb. This significantly impacts the page load speed and, therefore, your user experience.

In addition, it might also have a positive impact on your search ranking. Last year, [Google added a page experience](https://developers.google.com/search/blog/2021/04/more-details-page-experience) update to their search result ranking. We tested the impact of adding a Google Analytics script to a website vs. adding the Simple Analytics script. Our results show that [Google penalizes you for using Google Analytics](https://blog.simpleanalytics.com/google-penalizes-you-for-using-google-analytics). The difference in page load speed was ten basis points.

There is, however, still a difference between the scripts of Simple Analytics (3kb) and Plausible(>1kb). The impact is not as significant as with Google Analytics, but it is interesting to see the difference. We don't track our users, so we need to get more from the browser to provide the same website stats. For example, Plausible gets its unique page views from tracking IP hashes for 24 hours. We get our unique page views from the referrer domain. This happens in the frontend, whereas tracking IP hashes happens in the backend. Also, our time on page metric is calculated in the frontend. Therefore, our script needs to be bigger.

For lightweight enthusiasts, we do have a [compressed version of the script (1.6kb)](https://docs.simpleanalytics.com/light).

### 4.2 Open source

Plausible is open-source, meaning their source code is publicly available.  The data collection scripts of Simple Analytics are also open-source. They are [available on GitHub](https://github.com/simpleanalytics/scripts) for everybody to check and verify. For us, it's important that customers can review what we collect. The rest of our dashboard is not open-source. This might change in the future, but we are a small team and want to focus on more features for our current customers first.

### 4.3 Mini websites & Twitter referral traffic

Simple Analytics is privacy-first but simple-second. It's probably the only analytics tool that transforms [referral links into mini websites](https://docs.simpleanalytics.com/mini-websites). They are referral links but visualized in a screenshot of the link page.

<img src="https://docs.simpleanalytics.com/images/mini-websites-simple-analytics.gif" alt="Mini websites as referrers in Simple Analytics vs. Plausible" class="border" />
<p class="caption" markdown="1">
  Mini websites in Simple Analytics
</p>

Do you see those "t.co" referrals domains in Plausible or Google Analytics? We created a Twitter overview that shows you the exact tweets you got traffic from. Not with useless t.co links, but with useful and beautiful designed tweets.

{% include video.html slug="2022-03-39-tropical-analytics" paused="true" %}

<p class="caption">Our founder using Google Analytics.</p>

### 4.4 Goal conversions and event tracking

Event tracking is one of the most important features of Google Analytics. Website owners want to see where visitors are going and which action they take. Because Plausible takes a different approach than Simple Analytics, it can be more accurate with respect to conversions.

As mentioned above, Plausible uses IP hashes to track individual users (anonymously) for 24 hours. It is, therefore, able to attribute an action to a specific user (or at least it can retrace where this user came from). Simple Analytics does this differently. We don't track or collect any personal data, but we can still see what's happening and which actions visitors take in general. We base our event tracking on aggregate data or ''counts of clicks'.

Let's say you want to run a Facebook campaign and want to know how many visitors filled in a specific form. How can you measure the effectiveness of this with Simple Analytics? To be honest, Simple Analytics is not built for organizations that heavily rely on ads, but it is possible to evaluate the effectiveness of specific campaigns.

Let's say you create a specific landing page, which you direct your Facebook ad towards. You can use UTM codes to recognize traffic coming from the ad. In addition, you can also measure how many times the 'fill in form' button is clicked. It fires an event every time the button is clicked. Conversions will look like this:

<img src="https://assets.simpleanalytics.com/blog/why-simple-analytics-is-a-great-alternative-to-plausible/event-tracking-sa.png" alt="Event tracking Simple Analytics" class="border" />
<p class="caption" markdown="1">
  Event tracking Simple Analytics
</p>

## 5. Costs

Plausible is open source. This means that the source code is out there for anyone to host their own analytics. However, you need to be technical, and you still need to pay for your own hosting and make sure to keep the software up to date.

These are the paid solutions Plausible offers:

-   9$ Per month for up to 10,000 pageviews.
-   19$ Per month for up to 100,000 pageviews
-   69$ Per month for up to 1 million pageviews

Simple Analytics is not open source and only has paid options. The Starter plan and the Business Plan:

-   Starter Plan: 19$ for up to 100,000 page views per month.
-   Business plan: 59$ for up to 1 million page views per month.

We value long-term customers. Hence we give a huge discount to customers on a yearly plan. For the Starter Plan, we charge 108$ per year, which is 9$ per month.

## Why do we care

Adriaan started Simple Analytics four years ago to make the internet a little bit safer and provide an alternative to data-devouring machines like Google. We genuinely believe it can get actionable insights without using personal data or tracking mechanisms.

We built Simple Analytics not only for companies that want to comply with GDPR law but for organizations that care about their visitors. By supporting us in our mission, you are not only preserving your visitor's privacy but also supporting a small independent team of two. Feel free to [give us a try.](https://simpleanalytics.com/welcome)
