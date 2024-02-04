---
title: "Does Safari block Google Analytics? And Apple's privacy updates"
author_slug: iron
author: Iron Brands
excerpt: "Does Safari still work with Google Analytics after Apple's privacy updates? And will Safari ever block Google Analytics?"
image: https://assets.simpleanalytics.com/blog/does-safari-block-google-analytics-and-apple-privacy-updates/social-image-text.png
image_no_text: https://assets.simpleanalytics.com/blog/does-safari-block-google-analytics-and-apple-privacy-updates/social-image-no-text.png
related_posts:
  - /blog/website-analytics-without-cookies
  - /blog/less-is-more-data-minimization-can-help-your-business
  - /blog/vodafone-deutsche-telekom-to-introduce-persistent-user-tracking
  - /blog/google-analytics-performance-impact-using-google-lighthouse
last_modified_at: 2022-09-28
---

In June 2020, Apple launched a new 'Privacy Report' during their first digital [WWDC event](https://insiderpaper.com/apple-wwdc-livestream-online-start-time-watch/). This included new privacy guidelines and a summary of trackers blocked by Safari (an Apple product) on iOS, Big Sur, and iPadOS.

The new features caused some confusion among the attendants. From the presentation, it seemed that Safari blocked Google Analytics by default. However, the truth is a bit more nuanced.

So what was the fuss all about again, and what privacy updates have been implemented since? We’ll also touch upon the impact future privacy updates will have on the usability of tools like Google Analytics. What is the likelihood that Safari will ever block Google Analytics?

![Safari blocks Google Analytics](https://assets.simpleanalytics.com/blog/does-safari-block-google-analytics-and-apple-privacy-updates/privacy-report-marktplaats.png)
_Safari Privacy Report_

Let's dive in!

{{tableofcontents}}

## Safari does not block Google Analytics by default 

With the "Privacy Report," Apple added many new privacy features to help protect users from being tracked across the internet. In the presentation, Apple showed that Google Analytics was the most frequently blocked tracker. This made everyone assume that Safari is blocking Google Analytics from tracking website visitors by default. However, this was a false assumption, and the truth is a bit more complicated.

![Apple privacy report](https://assets.simpleanalytics.com/blog/does-safari-block-google-analytics-and-apple-privacy-updates/big-sur-safari-privacy-report.png)
_Apple Privacy Report presentation_

This was the screenshot shown during the event. Google Analytics is marked as a prevented tracker in the picture, which caused the confusion.

The first to react was analyst [Simo Ahava](https://twitter.com/SimoAhava) who explained what was really going on:

_"When the Safari screenshot from #WWDC says it prevents "http://google-analytics.com..." it likely means ITP flagged that domain as a cross-site tracker and restricts its access to third-party storage. NOT that it actually "blocks GA."_

## Blocking Third-Party Tracking Cookies

As more information surfaced, it became clear that Safari was not blocking Google Analytics but rather its third-party cookies.

- **First-party cookies** are stored by the domain (website) you visit.
- **Third-party cookies** are created by domains other than the one you visit directly, hence the name third-party.

If you want to freshen up your mind regarding first-party vs. third-party cookies, check our ["cookie article." ](/blog/what-are-internet-cookies)

The Intelligent Tracking Prevention in Safari 14 blocks cross-site tracking, limiting only portions in Google Analytics. Website owners should have no trouble seeing their website analytics, as it relies on first-party cookies. Google Analytics still functions as an analytics platform, but you can't use it for retargeting and other features that rely on cross-website tracking.

So Safari does not block Google Analytics, but Apple's "Privacy Report" did accelerate a privacy trend that is not stopping anytime soon.

![Safari blocks Google Analytics](https://assets.simpleanalytics.com/blog/does-safari-block-google-analytics-and-apple-privacy-updates/social-image-no-text.png)
_The privacy battle, who will win?_

## The impact of privacy updates

In the past year, we've [seen a crackdown on government bodies on the use of Google Analytics.](/blog/france-rules-google-analytics-to-be-in-conflict-with-gdpr-ruling) Privacy laws like GDPR, PECR & CCPA are getting stronger by the day, and organizations seem to care more and more about running their business ethically.

In addition, Apple is moving forward with its privacy operations. They recently added the App Tracking Transparency (ATT) feature in their iOS15, which runs on [72% of modern iPhones. ](https://developer.apple.com/support/app-store/)

The ATT consists of a pop-up that asks users if they want to be tracked when they open the app. Facebook announced that this new feature [will cost them 10 billion in ad revenue](https://www.cnbc.com/2022/02/02/facebook-parent-meta-fb-q4-2021-earnings.html) this year alone.

Next to that, Apple [launched a commercial](https://www.youtube.com/watch?v=NOXK4EVFmJY) showing a girl whose digital identity and belongings are sold off by an auctioneer. At the time of writing, it's 16 days old and already has 7,7 million views on Youtube.

Obviously, the video has some marketing angle to it. Still, the fact that the biggest company in the world has its marketing focus on privacy shows the importance and relevancy of digital privacy.

## Why you should move away from Google Analytics

As mentioned above, Safari does not block Google Analytics. You can still still see your website analytics. However, the privacy trend is not slowing down, and Google is just not moving with it.

{% include gif.html slug="thats-what-i-heard" alt="thats what I heard" width="480" height="343" color="#2b1f20" %}

### Phasing out of third-party cookies

If you use Google Analytics for cross-site tracking, retargeting and ad-serving, you should rethink your marketing practices. Not just from an ethical standpoint but because of the fact that even Google Chrome is phasing out third-party cookies next year. This is a good thing, but believe me, Google does not want to. The world is moving to a [cookieless era](/blog/website-analytics-without-cookies)in which digital privacy is at its core. There is a reason behind Apple upgrading its privacy protection features: People care about privacy!

### Google Analytics is sunsetting Universal Analytics

If you are used to Google Analytics, I can imagine don’t want to another tool.  The interface might not be user-friendly, but you know your way around and can get all the necessary information. Google Analytics is also free (although is it really free?), whereas alternatives are not, and the cost of switching to a new tool might just not be worth the hassle. However, a few months ago, Google stated that it is [sunsetting Universal Analytics in favor of GA4](/blog/google-to-sunset-universal-analytics-in-2023). This has been a subject of discussion as users are unhappy. This is probably the best moment to ethink your analytics provider, as you will need to start learning a new tool anyway.

### Google Analytics creates a blind spot

Although Google Analytics is the most powerful analytics tool there is, it will become more inaccurate. Internet users demand privacy, not by knocking on your door and asking for it, but by using tools that block Google Analytics. More and more internet users use ad-blockers or plugins that block Google Analytics scripts.

In addition, privacy laws have agreed that every website that uses cookies should display a cookie banner. When more and more website visitors disagree with your cookie setting, you will miss them in your Google Analytics data.

### There are Google Analytics alternatives out there

Organizations have taken so long to become more privacy-friendly because of the lack of privacy-friendly tools that are as good as non-privacy-friendly ones. You might want to check other tools if you just use Google Analytics to get insights on your website statistics. There are [alternatives to Google Analytics](/blog/why-simple-analytics-is-a-great-alternative-to-google-analytics) that are simpler to use, with a more straightforward dashboard that doesn't sell your visitor data to third parties.

## Final Thoughts 

Digital privacy is becoming increasingly important in our lives, and organizations have started recognizing this. Apple has made privacy one of its future core pillars. Its privacy features are hurting ad platforms like Google and Facebook and making their tools, such as Google Analytics, less powerful. We feel that privacy is a fundamental human right.

Also, more and more people are rightfully concerned about their privacy on the internet and are taking matters into their own hands by switching to privacy-centric apps or browsers.

Data protection authorities are also showing their teeth by declaring the use of Google Analytics unlawful in [Italy](https://www.simpleanalytics.com/blog/italy-declares-google-analytics-illegal), [Denmark](https://www.simpleanalytics.com/blog/denmark-declares-google-analytics-unlawful), [France](https://www.simpleanalytics.com/blog/france-rules-google-analytics-to-be-in-conflict-with-gdpr-ruling) & Austria. More EU member states are likely to follow in the coming months, as this was a coordinated effort on a European level.

In addition to the above, we feel that privacy is a fundamental human right, so we created Simple Analytics.

Simple Analytics is not impacted by privacy updates, like the one mentioned above by Apple; it only strengthens our case. We are cookieless by design and never collect any personal data.

We are EU-based. Fully GDPR compliant, and the data we collect is yours. YWe believe in creating an independent internet that is friendly to website visitors. If this resonates with you, feel free to [give us a try](https://simpleanalytics.com/welcome).
