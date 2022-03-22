---
title: Website analytics without cookies
author_slug: iron
author: Iron Brands
excerpt: "The future of web analytics is cookieless, but how does analytics work without cookies? Let's find out"
image: https://assets.simpleanalytics.com/blog/socials/google-kill-universal-analytics.png
lang: en
draft: true
---

It has been the talk of the town lately. "Google Analytics might be banned in Europe".

The DSB in Austria was the first to [openly question](https://noyb.eu/en/austrian-dsb-eu-us-data-transfers-google-analytics-illegal) the legal use of Google Analytics. Various popular news outlets such as Hacker News & [Techcrunch](https://techcrunch.com/2022/01/12/austrian-dpa-schrems-ii/) picked up on the news and spread the word.

Not so long after the DSB, their french counterpart, [CNIL, also stated](https://www.cnil.fr/en/use-google-analytics-and-data-transfers-united-states-cnil-orders-website-manageroperator-comply) that Google Analytics conflicts with GDPR.

Organizations, especially within the EU, are questioning themselves now if they could still use Google Analytics legally. And what happens if they can't? Will they lose all the valuable insights as well?

In other words: Will there be life after Google Analytics?

{% include gif.html slug="dont-be-so-dramatic" alt="Don't be so dramatic" width="320" height="320" color="#382a3a" %}

Let's find out 👇

1.  How does Google Analytics work?
    1.  Does Google Analytics use cookies?
    2.  Do you need a cookie banner when using Google Analytics?
    3.  Google Analytics without cookies?
2.  Website analytics without cookies
    1.  What data does Simple Analytics collect?
    2.  How can Simple Analytics count unique visitors?
    3.  Can you still track events and conversions?

# 1. How does Google Analytics work?

Google Analytics is by far the most used analytics tool on the planet. At least 86% of the websites that are using an analytics tool, are using Google Analytics. It's a free tool, but it comes at a cost.

To understand why Google Analytics has come under pressure lately, it's key to understand how Google Analytics works and what implications it brings.

## 1.1 Does Google Analytics use cookies?

If you install Google Analytics to track your website performance you need to set first-party cookies to:

- Identify unique visitors
- Identify unique sessions
- Identify traffic source information
- Determine the start and end of a session

Want to learn more about what cookies are? Check out this [blog post](https://blog.simpleanalytics.com/what-are-internet-cookies).

You can access the cookies when you open the developer toolbar (right-click + inspect). By navigating to the 'application' tab and clicking on 'cookies', you can see which cookies are used by the specific website.

<img src="https://assets.simpleanalytics.com/blog/cookies/indeed-cookies.png" alt="Cookies of Indeed.com inspected via browser" class="border" />
<p class="caption" markdown="1">
  Cookies of indeed.com inspected via browser
</p>

As you can see from the screenshot above (taken from the Indeed homepage), the name of the cookie is indicated as '\_ga'. The second arrow on the screenshot indicates the value:

GA.1.2.1680553188.1645472981

It consists of a version name, which is the first part, and a unique ID, which is the second part.

The version name: <mark>GA.1.2.</mark>

The unique identifier: <mark>1680553188.1645472981</mark>

The unique identifier consists of two parts. The first part is a randomly generated number. The second part is a timestamp for the first time the visitor visited the page. That way Google can identify whether someone is a unique visitor or not.

Whenever someone visits a website, Google Analytics looks for the cookie, which is provided by the web browser. If there is a cookie stored, Google knows that the visitor is not unique. If Google can't find a cookie, it means it's a first-time visitor that visited the website. This is how Google Analytics distinguishes between unique visitors and pageviews.

## 1.2 Do you need a cookie banner when using Google Analytics?

According to GDPR, websites need to get consent from those visitors to store a cookie on their device. Meaning, when you install Google Analytics you need to show a cookie banner to ask for consent. To ensure Google Analytics works in compliance with privacy regulations, you need to take the following steps:

1.  Don't store cookies if you don't have consent.

2.  Make sure Google Analytics cookies are only activated after users have given their consent

3.  Be transparent with regards to the details of the Google Analytics cookies you are using. According to privacy regulations, consent is only valid if it constitutes an informed decision. You need to explain what type of cookies you are using.

4.  Compile detailed information in your privacy policy. You need to include all Google Analytics cookies and other personal data tracking mechanisms in the privacy policy

5.  Turn on IP anonymization in your Google Analytics account and make sure that it uses pseudonymous identifiers.

Not only are cookies privacy-invasive (that's the reason for the cookie banner), but you will also lose data.

If a website visitor does not give consent to be tracked, the cookie won't be stored on the visitor's device. This means your website metrics are not as accurate as they may seem. Actually, the numbers you see in your dashboard are underperforming your actual numbers.

This is not only true for Google Analytics, but for every web analytics tool that uses cookies.

More and more people become aware of the fact that they are being tracked around the internet, meaning that it is very likely that fewer people will give consent. This results in less accurate data.

## 1.3 Can you use Google Analytics without cookies?

The short answer: Yes you can (whilst still not being compliant with GDPR-regulation)

<mark>The longer answer: Yes you can, but you probably don't want to</mark>

Google Analytics is a tool to show you how your website is performing by tracking certain metrics. For those metrics to show accurate results, Google Analytics needs cookies to be installed on your website. If you want to try using Google Analytics without cookies, you are left with a broken analytics tool.

If you are looking for website analytics without cookies, you should probably look at some alternative solutions.

{% include gif.html slug="mr-bean-eyebrows" alt="Rowan Atkinson as Mr. Bean with his classic eyebrows" width="150" height="135" color="#6e625f" %}

# 2. Website analytics without cookies

The biggest difference between website analytics with cookies and website analytics without cookies is the trade-off between privacy and data:

The deeper you want to analyse on the individual level, the less-privacy-friendly you will need to be.

## 2.1 What data does Simple analytics collect?

At Simple Analytics we lean heavily towards the privacy side of the trade-off.

After installing Google Analytics scripts for several years, Adriaan didn't feel quite right to pass on so much data to Google for free. So he came up with a solution to provide insights, without invading the privacy of website visitors.

This means that website visitors don't need to interact with an annoying cookie banner before they enter your website. It also means that we are ['out-of-the-box' compliant with GDPR ](https://docs.simpleanalytics.com/what-we-collect)

I hear you think... "This sounds good, but what data will I be missing? Can you still identify unique visitors if you don't use cookies? And can you still track events?

{% include gif.html slug="i-need-answers" alt="I need answers." width="500" height="281" color="#695a56" %}

Well... Yes, you can, but don't just take my word for it. [See for yourself](https://simpleanalytics.com/welcome).

## 2.2 How do we identify unique visitors?

We have to be honest here. [Calculating unique visitors](https://docs.simpleanalytics.com/explained/unique-visits) is a lot more difficult without cookies. As explained earlier in this post, Google Analytics can spot a unique visitor based on the fact if it has already placed a cookie or not.

Other "privacy-friendly" alternatives in the space, anonymize IP addresses to check for unique visitors, and while from a privacy perspective this is more privacy-friendly, it is still considered personal data.

We do it even better.

We use the referral domain to see if someone is a unique visitor. When a user navigates to your website, the browser sends information about the referrer along.

Looking at the illustration below. Let's say someone visits a certain website (randomwebsite.com) and from there navigates to your website (yourwebsite.com). The browser sends the referrer (randomwebsite.com) to yourwebsite.com. This referrer is very useful to figure out where traffic is coming from.

![](https://docs.simpleanalytics.com/images/referrer-visit.jpg)

When a user lands on your website without visiting another website, we record it as a unique visit:

![](https://docs.simpleanalytics.com/images/direct-visit.jpg)

## 2.3 Can you still track events?

It is one of the most common questions we get. With Simple Analytics it is still possible to track event counts. It is based on aggregate data, meaning that we can't collect data on individuals triggering the event.

You can add our automated events script or add your custom events to see your event counts. Based on the traffic to that specific page, we can estimate a conversion (and we are working on a user-flow section).

In addition, you can still use URL Parameters to see where your traffic is coming from. For example, if you want to see the traffic from a blog post or newsletter.

## 2.4 When should you consider a privacy-first alternative?

Ask yourself the question, what data do you really need? Do you really need to track every individual move of a website visitor? If that's the case, Simple Analytics might not be the tool for you.

We are here for companies that want to be part of the future. Companies that want to see the big picture while acting in the best interest of their visitors.

So if you are looking for a solution that is...

...GDPR-compliant 'out of the box'

...Cookieless by design

...Gives you the big picture

...And Simple to understand and use (see our [live dashboard](https://simpleanalytics.com/simpleanalytics.com))

You might want to give us a [try](https://simpleanalytics.com/welcome?plan=starter&interval=monthly).
