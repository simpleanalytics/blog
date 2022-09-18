---
title: "Simple Analytics for Marketers"
author_slug: iron
author: Iron Brands
excerpt: "Marketers guide for Simple Analytics, the privacy-first Google Analytics alternative"
image: https://assets.simpleanalytics.com/blog/2022-simple-analytics-for-marketers/social-image.png
image_no_text: https://assets.simpleanalytics.com/blog/2022-simple-analytics-for-marketers/social-image-no-text.png
draft: true
---

First paragraph

{% include gif.html slug="spy-kids-better-look-closer" alt="Spy Kids: Better look closer" width="300" height="201" color="#594748" %}

<img src="https://assets.simpleanalytics.com/blog/google-alternatives/google-analytics-dashboard.png" alt="Caption of the image" class="border-radius" />
<p class="caption" markdown="1">
  Caption of the image
</p>

Rest of the article

Simple Analytics is a privacy-friendly analytics tool that is cookieless by design and fully complies with GDPR. It provides actionable insights in a simple one-page dashboard without compromising the privacy of your website visitors.

Below we aim to answer the number one question concerning privacy-friendly analytics: "What's still possible for marketers?"

This question is understandable. More privacy means less data collection and less information to do the marketer's job. However, more privacy does not always mean fewer insights.

Google Analytics has come under fire lately (and for a good reason). Multiple EU countries have already banned it, and more EU members are expected to reach the same conclusion. Also, Google announced it will sunset Universal Analytics in favor of GA4 in May next year.

So now might be a good time to explore what privacy-friendly alternatives offer.

{% include gif.html slug="one-way-to-find-out" alt="one way to find out" width="480" height="480" color="#605441" %}

Let's dive in!

1.  Get actionable insights from your analytics
2.  Keep track of your ad campaigns with UTM tags
3.  Add Events to measure conversions
4.  Use APIs to build your own dashboards
5.  Integrate Simple Analytics with your favorite dashboarding tools
6.  Import Google Analytics data directly into your dashboard
7.  Share reports with your team
8.  Get accurate website traffic data
9.  Benchmark Google Analytics data
10. Improve your website's user experience
11. Improve your core web vitals
12. Comply with regulations

## 1. Get actionable insights from your analytics

We are called Simple Analytics for a reason. Retrieving actionable insights from Google Analytics can be painful. It provides an overkill of information by showing infinite menus and functions. We focus on what's important in a single-page dashboard that gives an accurate overview in seconds.

The dashboard shows...

... where your visitors are coming from and what pages they are visiting
... the number of visitors and pageviews for every page
... the average time users spend on your pages
... in which countries your visitors are based
... and which browsers and devices they use to visit your website

Everything in our dashboard is clickable. You can create a custom dashboard in seconds based on traffic source, country, or browser. These metrics can also be combined.

Do you want to know which browser is used the most by website visitors from the U.S. that navigate to a specific page? No problem.

Feel free to check this out yourself. We have a [live demo of our analytics](https://simpleanalytics.com/simpleanalytics.com) on our website to better understand all the available metrics.

## 2. Keep track of your ad campaigns with UTM tags

We determine where visitors are coming from based on the (referrer) previous page. This information is retrieved from the visitor's browser. However, it's also possible to override this using a custom referrer. This might come in handy when you want to track specific ad campaigns and is done by [adding a URL parameter](https://docs.simpleanalytics.com/how-to-use-url-parameters).

UTM tags are bits of text you can add to a link that tell Simple Analytics a little more information about each link.

We support the following codes:

-   UTM source (e.g.: utm_source=company-x)
-   UTM medium (e.g.: utm_medium=newsletter)
-   UTM campaign (e.g.: utm_campaign=march_01)
-   UTM content (e.g.: utm_content=button_red)
-   UTM term (e.g.: utm_term=shoes, this param is deprecated as it is intended to contain user-generated content)

The UTM tags will show up on the dashboard in the "Referrals" dropdown menu:

<img src="https://assets.simpleanalytics.com/blog/For%20marketers/utm-referrals.png" alt="utm-referrals" class="border-radius" />
<p class="caption" markdown="1">
</p>

## 3. Add events to measure conversions

Keeping track of conversions is important. In Simple Analytics, you can collect events such as downloads, sign-ups, and other outbound links. It is possible to fire events for any action taken by someone visiting your website. We ensure you can track how many website visitors sign up for your product or service.

We measure conversion by comparing two or more specific events. Like in the image below. For instance, If you want to know the relation between the number of pageviews (event 1) and the number of signups (event 2) in a specific period, we can measure this by comparing the two events.

<img src="https://assets.simpleanalytics.com/blog/For%20marketers/events-dashboard.png" alt="events dashboard" class="border-radius" />
<p class="caption" markdown="1">
</p>

To make it easier for non-developers, we created [an automated events script](https://docs.simpleanalytics.com/automated-events). This script collects events for downloads and outbound links and clicks on email links automatically. You can also create your own custom events if you want to get your hands dirty. [Here](https://docs.simpleanalytics.com/events) is how you can go about setting up your custom events.

## 4. Use APIs to build your own dashboards

Simple Analytics does not own your data. You do! That's why we care a lot about the interoperability of your data.

[Our APIs](https://docs.simpleanalytics.com/api) are a good example of that. Most analytics companies do not give you access to your raw data. We believe it should be easy for our customers to get their raw data out of our database. You should decide what you want to do with your data.

There are a few ways to interact with our API. We have the [Stats API](https://docs.simpleanalytics.com/api/stats) for aggregated data, the [Export API](https://docs.simpleanalytics.com/api/export-page-views) for raw level data, and the [Admin API](https://docs.simpleanalytics.com/api/admin) for changing users, websites, and other settings.

{Insert export video} → https://docs.simpleanalytics.com/api/helpers#generate-export-url

## 5. Integrate Simple Analytics with your dashboarding tools

In addition to our APIs, it's also easy to integrate Simple Analytics with your favorite dashboarding tools. Some customers use [Google Data Studio](https://docs.simpleanalytics.com/google-data-studio) or [Microsoft Power BI](https://docs.simpleanalytics.com/microsoft-power-bi) for building reports.

Because we care about privacy, we don't store any personal data. That's why we are comfortable enough to let customers choose to connect with Data Studio while Google or Microsoft can't abuse our customers' data or their visitors'. 

## 6. Import Google Analytics data directly into your dashboard

[Importing your Google Analytics](https://docs.simpleanalytics.com/import-google-analytics-data) into your Simple Analytics dashboard directly and not losing any historical data is possible.

[Google Analytics is shutting down](https://blog.simpleanalytics.com/google-to-sunset-universal-analytics-in-2023) its Universal Analytics properties in 2023. To keep this data, you can choose to import it into Simple Analytics. We built an import tool where you can import your data in just a few clicks.

With Simple Analytics, you can import Universal Analytics properties and Google Analytics 4 properties.

## 7. Share reports with your team

Analytics is a vital part of every organization. You need to know what's happening to navigate your business in the right direction. This becomes very hard to do without actionable insights from your analytics.

Sharing actionable insights among team members is crucial to get everyone on the same page.

Sharing insights in Google Analytics can be a painstaking process. Simple Analytics makes sharing insights easy. You can add team members to your Simple Analytics account and even make your analytics public to share it with just anyone.

In addition, we send [weekly or monthly email reports](https://docs.simpleanalytics.com/email-reports), so you don't have to check the dashboard all the time. You can add as many team members (or other stakeholders to receive these reports and never miss that traffic spike. It includes the top 5 referrers, and we compare them with the previous period. This indicates where your website is getting its traffic from and how those numbers might have changed.

<img src="https://assets.simpleanalytics.com/blog/For%20marketers/email-reports.png" alt="email reports" class="border-radius" />
<p class="caption" markdown="1">
</p>

## 8. Get accurate website traffic data

This sounds contradictory: "Track less and get more accurate data." But this is essentially true, and there are a few reasons for it:

**Cookie banners** 

Before visiting your website, every website visitor needs to interact with a cookiebanner. If the visitor does not consent to be tracked, you have no idea that this visitor has been on your website. More visitors will have visited your website than Google Analytics will show you. This discrepancy will only continue to grow as more and more visitors don't want to be tracked. If you use a privacy-friendly alternative that is cookieless by design, each actual website visit will be shown.

**Adblockers**

More and more internet users are using ad-blockers because website users demand more privacy. Most ad-blockers block the Google Analytics script. Visitors that have ad-blockers installed won't show up in your stats.

**Referral spam** 

Referral spam has been a big problem for Google Analytics. Referral spam looks like genuine traffic to your website, but it's actually fake. Spammy advertisers send fake visitors to your website in two ways:

-   Bot referral spam: Bots visiting your website and making Google Analytics register it
-   Ghost referral spam: Bots totally bypass your website and directly hit the Google Analytics server

At Simple Analytics, we built a [feature that directly hides referral spam](https://docs.simpleanalytics.com/hide-referral-spam) from your dashboard.

**Data sampling**

Google Analytics uses data sampling to save server capacity and keep costs down. Data sampling means that only a subset of your actual traffic is processed. From this subset, Google Analytics predicts what your total traffic would look like. This is a cost-effective way to estimate website analytics. However, it is not nearly as accurate. 

## 8. Benchmark Google Analytics data

It's no secret that Google Analytics is a really powerful tool that is very helpful for marketers to do their job. However, it comes with some caveats. The inaccurate data caveat, as explained above, might be a reason to use Google Analytics and Simple Analytics simultaneously.

Simple Analytics might not be the right solution if you want to track individual website visitors. We are a cookieless solution after all. Google Analytics does this, but it requires a cookiebanner, which makes your total website traffic numbers inaccurate. Therefore, we've seen multiple use cases that use Simple Analytics to get their topline analytics correct and use Google Analytics to dive deeper.

The fact that Simple Analytics is very lightweight means that you could easily run it next to Google Analytics or any other web analytics provider to see the differences. 

## 9. Improve your website's user experience

If you use Google Analytics on your website to track your website performance, you are obliged by law to provide a cookie banner and ask for consent. This means your website visitors must first interact with a cookie banner before entering your website.

With Simple Analytics, this is not necessary anymore. Your visitors don't need to be shown a cookie banner when navigating to your website. 

## 10. Improve your core web vitals

Simple Analytics improves your core web vitals. This is because Simple Analytics is a simple tool with a small script that needs to be installed on your website.

Analytics scripts differ in size, and the bigger the script, the higher the impact on page load time. Bigger scripts slow down websites. The Google Analytics script (45kb) is a 'heavyweight' among web analytics scripts. In comparison, Simple Analytics' script is only (3kb).

A smaller script makes your website faster. This has two main advantages. First, this will improve your SEO score, and second, this will enhance your user experience.

We ran a [performance test](https://blog.simpleanalytics.com/google-penalizes-you-for-using-google-analytics) using Google Lighthouse to show the actual impact. There is a difference of 10 basis points in website performance between Simple Analytics and Google Analytics.

<img src="https://assets.simpleanalytics.com/blog/For%20marketers/core-web-vitals.png" alt="lighthouse analytics comparison" class="border-radius" />
<p class="caption" markdown="1">
</p>

## 11. Comply with privacy regulations

Simple Analytics is fully compliant with privacy laws. Google Analytics is not. In some EU member states, using [Google Analytics is against the law](https://www.simpleanalytics.com/blog/italy-declares-google-analytics-illegal). Since it's a coordinated effort from multiple EU member states against Google Analytics, more countries are expected to reach the same conclusion as [France](https://www.simpleanalytics.com/blog/france-rules-google-analytics-to-be-in-conflict-with-gdpr-ruling), [Italy](https://www.gpdp.it/web/guest/home/docweb/-/docweb-display/docweb/9782874#english) & [Austria](https://noyb.eu/en/austrian-dsb-eu-us-data-transfers-google-analytics-illegal) did. The Netherlands is expected to conclude at the end of 2022.

An actionable [agreement between the EU & US](https://www.simpleanalytics.com/blog/eu-us-privacy-shield-2-0-is-again-a-political-show) is still far away, and even if we reach this point, you can argue how sustainable it really is with the privacy movement getting more and more steam. Using Simple Analytics that is 100% compliant with GDPR gets the headache out of the way once and for all.

## Try Simple Analytics

If you've read this far, it's maybe time for an introduction...

We are Adriaan & Iron, and we've built [Simple Analytics](https://www.simpleanalytics.com/) to help create a more independent web that is friendly to website visitors.

You can [try Simple Analytics for free](https://simpleanalytics.com/welcome) on your website for 14 days (no credit card required). Even in the case that you would need a bit more time to determine whether Simple Analytics is something you would like to use, just send us a message. You can reach us on Telegram, or you can use our [contact page](https://simpleanalytics.com/contact). We would love to hear from you and ensure you get the most out of Simple Analytics.
