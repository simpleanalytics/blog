---
title: Cookieless website analytics vs. Google Analytics
author_slug: iron
author: Iron Brands
excerpt: "The future of web analytics is cookieless, but how does analytics work without cookies? Let's find out."
image: https://assets.simpleanalytics.com/blog/socials/website-analytics-without-cookies.png
lang: en
last_modified_at: 2022-05-03
---

It has been the talk of the town lately. "Google Analytics might be banned in Europe."

The DSB in Austria was the first to [openly question](https://noyb.eu/en/austrian-dsb-eu-us-data-transfers-google-analytics-illegal) the legal use of Google Analytics. Various popular news outlets such as Hacker News & [TechCrunch](https://techcrunch.com/2022/01/12/austrian-dpa-schrems-ii/) picked up on the news and spread the word.

Not so long after the DSB, their french counterpart, [CNIL, also stated](https://www.cnil.fr/en/use-google-analytics-and-data-transfers-united-states-cnil-orders-website-manageroperator-comply) that Google Analytics conflicts with GDPR.

Organizations, especially within the EU, are questioning themselves now if they could still use Google Analytics legally. And what happens if they can't? Will they lose all the valuable insights as well?

In other words: Will there be life after Google Analytics?

{% include gif.html slug="dont-be-so-dramatic" alt="Don't be so dramatic" width="320" height="320" color="#382a3a" %}

Let's find out 👇

1.  [How does Google Analytics work?](#1-how-does-google-analytics-work)
    1.  [Does Google Analytics use cookies?](#11-does-google-analytics-use-cookies)
    2.  [Is Google Analytics using first or third-party cookies?](#12-is-google-analytics-using-first-or-third-party-cookies?)
    3.  [How long do Google Analytics cookies last?](#13-how-long-do-google-analytics-cookies-last?)
    4.  [Do you need a cookie banner when using Google Analytics?](#14-do-you-need-a-cookie-banner-when-using-google-analytics)
    5.  [Do you need to include Google Analytics cookies in your privacy policy](#15-do-you-need-to-include-google-analytics-cookies-in-your-privacy-policy)
    6.  [Can you use Google Analytics without cookies?](#13-can-you-use-google-analytics-without-cookies)
2.  [Website analytics without cookies](#2-website-analytics-without-cookies)
    1.  [What data does Simple Analytics collect?](#21-what-data-does-simple-analytics-collect)
    2.  [How can Simple Analytics count unique visitors?](#22-how-do-we-identify-unique-visitors)
    3.  [Can you still track events?](#23-can-you-still-track-events)
3.  [Cookieless web analytics vs. Cookie based web analytics](#3-cookieless-web-analytics-vs.-cookie-based-web-analytics)
4.  [When should you consider a privacy-first alternative?](#4-when-should-you-consider-a-privacy-first-alternative)

# 1. How does Google Analytics work?

Google Analytics is by far the most used analytics tool on the planet. At least 86% of the websites that use an analytics tool use Google Analytics. It's a free tool, but it comes at a cost.

To understand why Google Analytics has come under pressure lately, it's key to know how it works and what implications it brings.

## 1.1 Does Google Analytics use cookies?

If you install Google Analytics to track your website performance, you need to set first-party cookies to:

- Identify unique visitors
- Identify unique sessions
- Identify traffic source information
- Determine the start and end of a session

Want to learn more about what cookies are? Check out this [blog post](https://blog.simpleanalytics.com/what-are-internet-cookies).

You can access the cookies when you open the developer toolbar (right-click + inspect). By navigating to the 'application' (or 'storage') tab and clicking on 'cookies,' you can see which cookies are used by the specific website.

<img src="https://assets.simpleanalytics.com/blog/cookies/indeed-cookies.png" alt="Cookies of Indeed.com inspected via browser" class="border" />
<p class="caption" markdown="1">
  Cookies of indeed.com inspected via browser
</p>

As you can see from the screenshot above (taken from the Indeed homepage), the cookie's name is indicated as '\_ga'. The second arrow on the screenshot indicates the value:

GA.1.2.1680553188.1645472981

It consists of a version name, the first part, and a unique ID, which is the second part.

The version name: <mark>GA.1.2.</mark>

The unique identifier: <mark>1680553188.1645472981</mark>

The unique identifier consists of two parts. The first part is a randomly generated number. The second part is a timestamp for the first time the visitor visited the page. That way, Google can identify whether someone is a unique visitor or not.

Whenever someone visits a website, Google Analytics looks for the cookie, which is provided by the web browser. If there is a cookie stored, Google knows that the visitor is not unique. If Google can't find a cookie, it means it's a first-time visitor that visited the website. This is how Google Analytics distinguishes between unique visitors and pageviews.

## 1.2 Is Google Analytics using first or third-party cookies?

Google Analytics uses first-party cookies. The difference is that first-party cookies are only issued when the user is directly using the website. The website that issues the cookies is also to only one that can read them.

In contrast, third-party cookies are issued by other websites than the one you are visiting. They are mainly used for remarketing purposes.  If you see ads from a website you visited in the past, it means that third-party cookies are tracking you.

## 1.3 How long do Google Analytics cookies last?

Both first and third-party cookies can be used with or without an expiration date. Cookies that are set with an expiration date are called persistent cookies. They stay on your device even after you close the web browser. Cookies without expiration date are called temporary cookies and are removed after you end your web session.

_ga is the main cookie for Google Analytics. It's a persistent cookie that stays for two years(!). However, you can change the cookie's duration to, for example, one year by following these steps.

You can overwrite the default of two years directly in the script (if you have an old Google Analytics script on your website). All you need to do is add the following 'cookieExpires' parameter to the script that issues the cookie: {'cookieExpires': 31536000}. The value here is noted in seconds and precisely a year.

You can also change it in Google Tag Manager, which is even easier:

-   Navigate to the Google Analytics Page View Tag
-   Check this box: *Enable overriding settings in this tag*
-   Click on: *open more settings*
-   Open *Fields to Set*
-   Click on: *Add Field* and fill out the two fields below. Indicate 31536000 in the value box to change the duration to one year.

## 1.4 Do you need a cookie banner when using Google Analytics?

According to GDPR, websites need to get consent from those visitors to store a cookie on their device. When you install Google Analytics, you need to show a cookie banner to ask for consent. To ensure Google Analytics works in compliance with privacy regulations, you need to take the following steps:

1. Don't store cookies if you don't have consent.

2. Make sure Google Analytics cookies are only activated after users have given their consent

3. Be transparent regarding the details of the Google Analytics cookies you are using. According to privacy regulations, consent is only valid if it constitutes an informed decision. You need to explain what type of cookies you are using.

4. Compile detailed information in your privacy policy. You need to include all Google Analytics cookies and other personal data tracking mechanisms in the privacy policy

5. Turn on IP anonymization in your Google Analytics account and make sure that it uses pseudonymous identifiers.

Not only are cookies privacy-invasive (that's the reason for the cookie banner), but you will also lose data.

If a website visitor does not consent to be tracked, the cookie won't be stored on the visitor's device. This means your website metrics are not as accurate as they may seem. The numbers you see in your dashboard are underperforming your actual numbers.

This is true for Google Analytics and for every web analytics tool that uses cookies.

More and more people become aware that they are being tracked around the internet, meaning that it is very likely that fewer people will give consent. This results in less accurate data.

## 1.5 Do you need to include Google Analytics cookies in your privacy policy

If your website issues Google Analytics cookies, you need to include this in your privacy policy. By law, you must be transparent about the cookies your website issues. If third-party cookies are issued, you need to address this separately in your privacy policy. It is also against Google's terms & conditions not to disclose that you are using cookies. If this is not addressed in your privacy policy, you illegally use Google Analytics.

## 1.6 Can you use Google Analytics without cookies?

The short answer: Yes, you can (while still not being compliant with GDPR-regulation)

<mark>The longer answer: Yes, you can, but you probably don't want to</mark>

Google Analytics is a tool to show you how your website is performing by tracking specific metrics. For those metrics to show accurate results, Google Analytics needs cookies to be installed on your website. If you want to try using Google Analytics without cookies, you are left with a broken analytics tool.

If you are looking for website analytics without cookies, you should probably look at some alternative solutions.

{% include gif.html slug="mr-bean-eyebrows" alt="Rowan Atkinson as Mr. Bean with his classic eyebrows" width="150" height="135" color="#6e625f" %}

# 2. Website analytics without cookies

The biggest difference between website analytics with cookies and website analytics without cookies is the trade-off between privacy and data:

The deeper you want to analyze on the individual level, the less-privacy-friendly you will need to be.

## 2.1 What data does Simple analytics collect?

At Simple Analytics, we lean heavily towards the privacy side of the trade-off.

After installing Google Analytics scripts for several years, Adriaan, our founder, didn't feel quite right to pass on so much data to Google for free. So he came up with a solution to provide insights without invading the privacy of website visitors.

This means that website visitors don't need to interact with an annoying cookie banner before they enter your website. It also means that we are ['out-of-the-box' compliant with GDPR ](https://docs.simpleanalytics.com/what-we-collect)

I hear you think... "This sounds good, but what data will I be missing? Can you still identify unique visitors if you don't use cookies? And can you still track events?

{% include gif.html slug="i-need-answers" alt="I need answers." width="500" height="281" color="#695a56" %}

Well... Yes, you can, but don't just take my word for it. [See for yourself](https://simpleanalytics.com/welcome).

## 2.2 How do we identify unique visitors?

We have to be honest here. [Calculating unique visitors](https://docs.simpleanalytics.com/explained/unique-visits) is a lot more difficult without cookies. As explained earlier in this post, Google Analytics can spot a unique visitor based on the fact if it has already placed a cookie or not.

Other "privacy-friendly" alternatives in the space anonymize IP addresses to check for unique visitors. While from a privacy perspective, this is more privacy-friendly, it is still considered personal data.

We do it even better.

We use the referral domain to see if someone is a unique visitor. When a user navigates to your website, the browser sends information about the referrer along.

Let's look at the illustration below. Someone visits a particular website (randomwebsite.com) and navigates to your website (yourwebsite.com). The browser sends the referrer (randomwebsite.com) to yourwebsite.com. This referrer is very useful to figure out where traffic is coming from.

![](https://docs.simpleanalytics.com/images/referrer-visit.jpg)

When a user lands on your website without visiting another website, we record it as a unique visit:

![](https://docs.simpleanalytics.com/images/direct-visit.jpg)

## 2.3 Can you still track events?

It is one of the most common questions we get. With Simple Analytics, it is still possible to track event counts. It is based on aggregate data, meaning that we can't collect data on individuals triggering the event.

You can add our automated events script or add your custom events to see your event counts. We can estimate a conversion based on the traffic to that specific page (and we are working on a user-flow section).

In addition, you can still use URL Parameters to see where your traffic is coming from. For example, if you want to see the traffic to a blog post or newsletter.

# 3 Cookieless web analytics vs. Cookie-based web analytics

The general take on cookieless web analytics tools is that you trade more privacy for fewer data. This is true because you collect fewer data points. However, it does not necessarily mean that analytics without cookies is less accurate. [Cookie-based web analytics tools are not bulletproof.](https://blog.simpleanalytics.com/why-simple-analytics-is-a-great-alternative-to-google-analytics)

**The use of adblockers affects your Google Analytics data**.

Adblockers block Google Analytics scripts. They prohibit the issuance of cookies on your device. Adblocker users visiting your website will be missed by Google Analytics.

The use of adblockers is rising. Adblock, a popular adblocking tool, [counted 735 million (!) users in 2019](https://www.statista.com/statistics/435252/adblock-users-worldwide/) and grew significantly among young people. Internet users are getting more aware of their digital fingerprints and the importance of digital privacy. This will only be accelerated in the future.

Adblockers can block the Simple Analytics script (however, to a lesser extent). We have created an adblocker bypass to ensure that we are not blocked and that you get the complete picture.

**Cookie banners allow visitors to opt-out of your Google Analytics data**

When using Google Analytics, you need to display a cookie banner on your website. Next to the fact that cookie banners hinder your user experience, they also affect your analytics.

Visitors indicating they do not want to be tracked will not be visible to Google Analytics. You will miss this data. [Research](https://www2.deloitte.com/be/en/pages/technology-media-and-telecommunications/topics/digital-consumer-trends-2020/data-privacy-awareness.html) suggests that most visitors still consent without even reading the cookie statement. However, this is about to change. Privacy laws are hammering down on consent practices. [Google is introducing new options](https://blog.google/around-the-globe/google-europe/new-cookie-choices-in-europe/) to reject tracking cookies.

It has been straightforward to give consent and accept cookies by pressing a button. However, indicating that you don't want to be tracked has been extremely difficult. You need to open the settings and configure multiple pages. This is also why most internet users 'just' give consent to not deal with the hassle. If saying 'no' becomes as easy as saying 'yes,' we expect fewer people to give consent.

Effectively, this means less accurate data in the Google Analytics dashboard. This is not an issue with Simple Analytics, as you don't need to ask for consent. We do not use cookies. Therefore, our page views are more accurate than page views in Google Analytics.

**Internet users removing their cookies are miscounted as unique visitors**

After removing their cookies, Google Analytics will mistakenly report returning visitors as unique visitors. As privacy awareness grows, more internet users will often remove their cookies. This will result in less accurate data concerning unique visitors in Google Analytics.

**Internet browsers block third party cookies**

Multiple browsers such as Safari and Brave [don't allow the use of third-party cookies](https://blog.simpleanalytics.com/what-are-internet-cookies), and even Google Chrome will stop supporting third-party cookies in 2023. Brave is a new kid on the block and identifies itself as the "anti-advertising" browser." Brave users can block ads and first-party cookies as well. It currently has [50 million monthly active users](https://brave.com/2021-recap/) and is growing rapidly. Another indication that the future will be cookieless.

# 4. When should you consider a privacy-first web analytics tool?

Ask yourself the question, what data do you really need? Do you need to track every individual move of a website visitor? If that's the case, Simple Analytics might not be your tool.

We are here for companies that want to be part of the future. Companies that want to see the big picture while acting in the best interest of their visitors.

So if you are looking for a solution, that is...

...GDPR-compliant 'out of the box'

...Cookieless by design

...Gives you the big picture

...And Simple to understand and use (see our [live dashboard](https://simpleanalytics.com/simpleanalytics.com))

You might want to give us a [try](https://simpleanalytics.com/welcome?plan=starter&interval=monthly).
