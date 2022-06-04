---
title: "Does Safari block Google Analytics? And Apple's privacy updates"
author_slug: iron
author: Iron Brands
excerpt: "Does Safari still work with Google Analytics after Apple's privacy updates? And what does the future hold.
image: https://blog.simpleanalytics.com/images/
draft: true
---

In June 2020, Apple launched a new 'Privacy Report' during their first digital [WWDC event](https://insiderpaper.com/apple-wwdc-livestream-online-start-time-watch/). This included new privacy guidelines and a summary of the number of trackers that would be blocked in Safari (an Apple product) on iOS, Big Sur, and iPadOS.

The new features caused some confusion among the attendants. From the presentation, it seemed that Safari blocked Google Analytics by default. However, the truth is a bit more nuanced.

So what was the fuss all about again, and what privacy updates have been implemented since? And what If we are moving to a more privacy-friendly internet, new privacy updates seem inevitable as well. What will these future privacy updates have on the usability of tools like Google Analytics? 

<img src="https://assets.simpleanalytics.com/blog/does-safari-block-google-analytics-and-apple-privacy-updates/safari-stop-tracking-privacy-report.png" alt="safari block google analytics" class="border" />
<p class="caption" markdown="1">
  Safari Privacy Report
</p>

Let's dive in!

1.  Safari does not block Google Analytics by default.
2.  Blocking third-party cookies vs. first-party cookies
3.  The future of privacy updates
4.  Why you should stop using Google Analytics

## 1. Safari does not block Google Analytics by default 

With the "Privacy Report," Apple added a lot of new privacy features to help protect users from being tracked across the internet. In the presentation, Apple showed that Google Analytics was the most frequent blocked tracker. This made everyone assume that Safari is blocking Google Analytics from tracking website visitors by default. However, this was a false assumption, and the truth is more complicated.

<img src="https://assets.simpleanalytics.com/blog/does-safari-block-google-analytics-and-apple-privacy-updates/does-google-block-safari.png" alt="Apple privacy report" class="border" />
<p class="caption" markdown="1">
  Apple Privacy Report presentation
</p>

This was the screenshot shown during the event. Google Analytics is marked as a prevented tracker in the picture, which caused the confusion.

The first to react was analyst [Simo Ahava](https://twitter.com/SimoAhava) who explained what was really going on:

*"When the Safari screenshot from #WWDC says it prevents "http://google-analytics.com..." it likely means ITP flagged that domain as a cross-site tracker and restricts its access to third-party storage. NOT that it actually "blocks GA."*

## 2. Blocking Third-Party Tracking Cookies

As more information surfaced, it became clear that Safari is not entirely blocking Google Analytics by default but rather third-party cookies.

-   **First-party cookies** are stored by the domain (website) you are visiting directly.
-   **Third-party cookies** are created by domains other than the one you are visiting directly, hence the name third-party.

If you want to freshen up your mind regarding first-party vs. third-party cookies, check our ["cookie article." ](https://blog.simpleanalytics.com/what-are-internet-cookies)

The Intelligent Tracking Prevention in Safari 14 blocks cross-site tracking, limiting only portions in Google Analytics. Website owners have no trouble seeing their website analytics, as these are considered first-party cookies. Google Analytics still functions as an analytics platform, but you can't use it for retargeting and other features where you need cross-website tracking.

Safari does not block Google Analytics. However, Apple's "Privacy Report" started a privacy trend that is getting more and more steam. 

## 3. The future of privacy updates

In the past year, we've [seen a crackdown on government bodies on the use of Google Analytics.](https://blog.simpleanalytics.com/france-rules-google-analytics-to-be-in-conflict-with-gdpr-ruling) Privacy laws like GDPR, PECR & CCPA are getting stronger by the day, and organizations seem to care more and more about running their business ethically.

In addition, Apple is moving forward with its privacy operations. They recently added the App Tracking Transparency (ATT) feature in their iOS15, which runs on [72% of modern iPhones. ](https://developer.apple.com/support/app-store/)

The ATT consists of a pop-up that asks users if they want to be tracked when they open the app. Facebook announced that this new feature [will cost them 10 billion in ad revenue](https://www.cnbc.com/2022/02/02/facebook-parent-meta-fb-q4-2021-earnings.html) this year alone.

Next to that, Apple [launched a commercial](https://www.youtube.com/watch?v=NOXK4EVFmJY) that shows a girl whose digital identity and belongings are sold off by an auctioneer. At the time of writing, it's 16 days old, and it has 7,7 million views on Youtube.

Obviously, the video has some marketing purposes to it. Still, the fact that the biggest company in the world has its marketing focus on privacy shows the importance and relevancy of digital privacy.

## 4. Why you should stop using Google Analytics

As mentioned above, Safari does not block Google Analytics by default. You can still use it without worrying about gaps in your analytics. However, the privacy trend is not slowing down, and Google is just not moving with it.

{% include gif.html slug="thats-what-i-heard" alt="thats what I heard" width="480" height="343" color="#2b1f20" %}

### 1. Phasing out of third party cookies

If you use Google Analytics for cross-site tracking, retargeting and ad-serving, you should genuinely rethink your marketing practices. Not just from an ethical standpoint, but even Google Chrome is phasing out third-party cookies. This is a good thing, but believe me, Google is forced to do this. The world is moving to a [cookieless era](https://blog.simpleanalytics.com/website-analytics-without-cookies). There are reasons behind Apple upgrading its protection of privacy. The most important is that people value privacy, so focusing on it with your site and business will create happy users. 

### 2. Google Analytics is sunsetting Universal Analytics

If you are used to Google Analytics, I can imagine you'll want to stick with them.  The interface might not be very user-friendly, but you know your way around and can get all the info you need. Google Analytics is also free (although is it really free?), whereas alternatives are not, and the cost of switching to a new tool is just not worth the hassle. However, Google broke the news a few months ago that it's [sunsetting Universal Analytics in favor of GA4](https://blog.simpleanalytics.com/google-to-sunset-universal-analytics-in-2023). There has been a lot of commotion about the change as users are clearly not happy. This is probably the best moment to ditch Google Analytics for good.

### 3. Google Analytics creates a blind spot

Although Google Analytics is the biggest data devouring machine there is, it will get more and more inaccurate over time. Internet users demand privacy, not by knocking on your door and asking for it, but by using tools that block Google Analytics. More and more internet users use ad-blockers or plugins that block Google Analytics scripts.

In addition, privacy laws have agreed that every website that uses cookies should display a cookie banner. When more and more website visitors disagree with your cookie setting, you will miss them in your Google Analytics data. This is becoming a trend and makes Google Analytics highly inaccurate over time. 

### 4. There are Google Analytics alternatives out there

The main reason organizations have taken so long to become more privacy-friendly is the lack of privacy-friendly tools that are as good as the non-privacy-friendly ones.  If you just use Google Analytics to get insights on your website statistics, you might want to check other tools. There are [alternatives to Google Analytics](https://blog.simpleanalytics.com/why-simple-analytics-is-a-great-alternative-to-google-analytics) that are simpler to use, with a more straightforward dashboard that doesn't sell your visitor data to third parties.

Why do we care? 
----------------

[Simple Analytics](https://simpleanalytics.com/) is a privacy-first Google Analytics alternative that provides the insights you need while being 100% GDPR compliant. We are a small independent team that cares about privacy. We feel that privacy is a fundamental human right. And, more and more people are rightfully concerned about their privacy on the internet. That's why they switch to privacy-centric apps or browsers. We designed just that.

<img src="https://assets.simpleanalytics.com/blog/google-alternatives/simpleanalytics-dashboard-top.png" alt="Simple Analytics dashboard" class="border" />
<p class="caption" markdown="1">
  Simple Analytics dashboard
</p>

Instead of selling your visitor data to Google Analytics and supporting the biggest advertising company in the world, you can choose to support a small but driven team doing the right thing.

Simple Analytics is not impacted by privacy updates, like the one mentioned above by Apple; it only strengthens our case. We are cookieless by design and never collect any personal data.

We are EU-based. Fully GDPR compliant, and the data we collect is yours. You are in control. We don't try to make financial gains through data exploitation. That's why more than 600 privacy-focused companies and governments use Simple Analytics. [Give us a try](https://simpleanalytics.com/welcome).
