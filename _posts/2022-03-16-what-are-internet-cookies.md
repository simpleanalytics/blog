---
title: What are internet cookies?
author_slug: iron
author: Iron Brands
excerpt: "Your internet behavior is tracked by cookies. What are they? And what type of cookies are there?"
image: https://assets.simpleanalytics.com/blog/cookies/what-are-internet-cookies.png
related_posts:
 - /blog/website-analytics-without-cookies
 - /blog/why-its-time-to-move-away-from-google-analytics
 - /blog/why-simple-analytics-is-a-great-alternative-to-google-analytics
 - /blog/does-safari-block-google-analytics-and-apple-privacy-updates
lang: en
---

You are being watched and you probably know that. Your internet behavior is being tracked. When you visit a website to shop for a new pair of jeans, it might be very possible you see ads for those jeans on your Facebook feed later on.

Internet tracking mechanisms exist and we call them cookies. There are different types of cookies, which have different functions and have a varying magnitude of impact on privacy invasiveness.

The information in this blog is to provide you with an introduction to cookies and tracking technologies.

{% include gif.html slug="spongebob-eating-cookies" alt="Spongebob eating cookies from the internet" width="480" height="324" color="#73775d" %}

1.  [What are cookies?](#1-what-are-cookies)
2.  [What's the difference between first-party and third-party cookies?](#2-whats-the-difference-between-first-party-and-third-party-cookies)
    1. [First-party cookies](#21-what-are-first-party-cookies)
    2. [Third-party cookies](#22-what-are-third-party-cookies)
3.  [What is fingerprinting?](#3-what-is-fingerprinting)
4.  [Which browsers disable third-party cookies?](#4-which-browsers-disable-third-party-cookies)
    1. [Safari](#safari-apple)
    2. [Firefox](#firefox-mozilla)
    3. [Chrome](#chrome-google)
    4. [Edge](#edge-microsoft)
    5. [Brave](#brave)
5.  [Do I need a cookie banner?](#5-do-i-need-a-cookie-banner)

## 1\. What are cookies?

Cookies are bits of data in the form of text that can identify your computer as you use your computer network. When you visit a website, the cookie is sent to your computer and stored in your web browser.

The information inside the cookie is created by a server upon your connection. The data is labeled with a specific ID so that whenever the cookie is exchanged again between your computer and the server, the server knows what information to serve to you.

This is how websites remember your login details or language preferences when you return to the site.

## 2\. What's the difference between first-party and third-party cookies?

Not all cookies are bad. Cookies can be functional as well. There are different types of cookies, but we can divide them into two categories: first-party cookies and third-party cookies.

## 2.1 What are first-party cookies?

A first-party session cookie or a ‘temporary cookie’ only retains information about the user, as long as the user is on the website. Once the browser is closed, cookies are deleted.

Let's say, you are shopping online and you put multiple products from multiple pages in your shopping cart. The cookie makes sure that whenever you want to check out, the shopping cart is filled with the items you clicked during your session.

A website that remembers your login and password is using a first-party cookie as well, this time it's a ‘tracking cookie’. The information in the cookie will be stored for a longer period and makes sure that you don’t have to fill in your password every time you visit the website. However, they must be deleted after a certain time. Most likely after two years. However, privacy regulators and internet browsers are shortening the time a cookie can be stored legally.

<mark>First-party cookies are installed directly by the website you are visiting.</mark>

They remember language settings, shopping carts, login/passwords, and serve other functional purposes to enhance the user experience.

## 2.2 What are third-party cookies?

Third-party cookies are a different species. They are used by marketers to ensure that their products or services are targeted at the right audience. They can track visitors across multiple domains, making a richer picture of user behavior.

_Third-party cookies are installed by third parties like Google and Facebook on websites to serve another purpose, namely collecting as much information on website visitors with commercial intent._

Most likely everyone has seen Facebook ads of products or websites they visited in the past. That's because of third-party cookies. Those third-party cookies can be activated if a website, for example, uses the Facebook 'like button' on their page or have Google Analytics installed. This allows those companies to store third-party cookies on your device. Big tech is watching you.

{% include gif.html slug="eyes-on-you" alt="I have my eyes on you" width="220" height="122" color="#7c635a" %}

## 3\. What is fingerprinting?

Another technology used to track visitors is called fingerprinting. It is a way of profiling internet users based on their hardware and software preferences. It is used by companies to identify who you are based on the specific setup you use to surf the internet. It is considered to be as invasive as cookie-based tracking methods.

Websites making use of fingerprinting technologies can track a visitor for months, even when you have cleared all your cookies and browser storage.

Even though everyone agrees that fingerprinting is harmful, its usage has gone up in recent years. To see what data we collect at Simple Analytics, visit [this page](https://docs.simpleanalytics.com/what-we-collect).

## 4\. Which browsers disable third-party cookies?

The rollout of privacy regulations such as the [GDPR](https://gdpr-info.eu/) & [PECR](https://ico.org.uk/for-organisations/guide-to-pecr/what-are-pecr/) has increased public awareness of the privacy invasiveness of cookies and other tracking technologies. In response to this, web browsers have started to add privacy protections for their users. The protections are put in place to block certain types of cookies or other tracking technologies. However, the degree of strictness between web browsers goes from very strict, to no protection at all.

### Safari (Apple)

Safari is considered to be very strict. It has blocked third-party cookies completely, which means that Google and Facebook are not able to track a visitor across multiple websites. In addition, persistent cookies such as the first-party tracking cookies only last for 7 days. If the visitor arrives on your site from a platform with cross-tracking abilities, the cookie lasts only for 1 day. This makes it difficult to attribute a visitor to a specific marketing campaign. [Check out their full cookie policy](https://support.apple.com/en-za/guide/safari/sfri11471/mac).

### Firefox (Mozilla)

Firefox is more 'medium-to-strict'. Third-party cookies are blocked, which means that tracking visitors across multiple sites is not possible. It will be more difficult to create remarketing campaigns, but understanding the impact of the campaigns can still be done quite accurately as the Google Analytics script is still allowed to run. [Check out their cookie policy](https://support.mozilla.org/en-US/kb/third-party-cookies-firefox-tracking-protection).

### Chrome (Google)

It will be no surprise that Google Chrome is the least strict internet browser. Google announced that it will block third-party cookies in the next two years. Google's business model is too reliant on advertising that it needs to strike a balance between what advertisers want and what users demand. The bottom line is that Google Chrome, allows all forms of cookies to be stored on your device. [Check out their cookie policy](https://policies.google.com/technologies/cookies?hl=en-US).

### Edge (Microsoft)

Microsoft Edge is viewed to be 'medium-to-strict' as well. It blocks third-party cookies but leaves analytics tools unaffected. Their default setting does not stop analytics tools from setting cookies and also the longevity is not limited.

Most browsers are aware of the fact that third-party cookies are bad. Only Google Chrome is not (yet) blocked third-party cookies and this is important to note as Chrome is by far the biggest (desktop) web browser in terms of market share. [Check out their cookie policy](https://support.microsoft.com/en-us/windows/microsoft-edge-browsing-data-and-privacy-bb8174ba-9d73-dcf2-9b4a-c582b4e640dd).

### Brave

Brave has come out of beta in the fall of 2019 and introduced itself as the “anti-advertising” browser. It strips ads of websites and lets the user opt-in to its own set of anonymized advertising. Its offering is fully focused on being a privacy-first browser.

By default, it blocks third-party cookies and other tracking mechanisms. You can block ads and first-party cookies manually. Protecting against fingerprinting is also included in its toolbox. [Check out their cookie policy](https://support.brave.com/hc/en-us/articles/360050634931).

<img loading="lazy" class="border" style="padding: 1rem;" src="https://assets.simpleanalytics.com/blog/cookies/marketshare-browsers.png" alt="">
<p class="caption" markdown="1">Market share of internet browsers desktop (source [Statista](https://www.statista.com/statistics/544400/market-share-of-internet-browsers-desktop/))</p>

Google Chrome has declared that it will be phasing out third-party cookies by 2022. However, they have already [postponed the deadline](https://blog.google/products/chrome/updated-timeline-privacy-sandbox-milestones/) to the end of 2023....Personally, I have a hard time believing that they are actually going to do this, as this will have huge consequences for their business model.

We'll have to see how this plays out, but for now, if you don't want to be tracked by third-party cookies. Stay away from Google Chrome. Go for Brave, or at least stay away from Google Chrome.

## 5\. Do I need a cookie banner?

As a website owner, if you want to track individual visitor behavior and you decide to install cookies on your user's device, you need to comply with certain privacy regulations.

First of all, you should ask yourself the question of why you actually want to track visitors individually. There are numerous ways to get insights into website statistics or user behavior without tracking personally identifiable information.

If you decide to move forward with tracking your users, you are obliged to:

1.  <mark>Tell that they installed cookies and clarify which ones they use</mark>
2.  <mark>Explain what the cookies are doing and why</mark>
3.  <mark>Get the user's consent to store a cookie in their browser</mark>

You can provide his information in a cookie banner, which will be shown when a first-time visitor visits your website. It informs the visitor about the cookies and trackers your website uses and asks for the visitors' consent to store cookies in their browser.

Next to the fact that you need to ask yourself whether you actually need this data, cookie banners are just annoying and have an impact on the user experience of your website. To visit your website, visitors first have to interact with the cookie banner.

For example, If you use Google Analytics on your website to track your website performance, you are obliged by law to provide a cookie banner and ask for consent. Whereas with Simple Analytics, you don't. We collect data to provide you with website performance metrics without you having to use cookies or fingerprinting technologies.

Then again, the question arises whether you need all the data Google Analytics is providing. I don't think so if you see what insights we can show you with Simple Analytics.

But don't take our word for it. See for yourself and [give us a try](https://simpleanalytics.com/welcome) or... [check-out our dashboard](https://simpleanalytics.com/simpleanalytics.com).

{% include gif.html slug="check-this-out" alt="Check this out!" width="498" height="280" color="#212a27" %}
