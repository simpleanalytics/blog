---
title: You are getting fooled by Google Analytics' time on page metric
author_slug: iron
author: Iron Brands
excerpt: "Time on page is an important metric to track. It gives you insights into how engaging your content is and if people are finding what they are looking for. But have you ever wondered how google comes up with the data you see in your dashboard?"
image: https://assets.simpleanalytics.com/blog/you-are-getting-fooled-by-google-analytics-time-on-page-metric/social.png
lang: en
---

Website analytics are key. At least [56% of the websites](https://w3techs.com/technologies/overview/traffic_analysis) worldwide are using some sort of analytics tool to track visitor metrics. [Google Analytics](https://analytics.google.com/analytics/web/) is by far the most used one (85%), and chances are high, you are using it too.

_Time on page_ is a critical metric to track. It gives you insights into how engaging your content is and if people are finding what they are looking for. But have you ever wondered how google comes up with the data you see in your dashboard?

We’ve deconstructed how Google calculates the time on page metric and what’s wrong with it in this post.

{% include gif.html slug="something-fishy" alt="Something fishy..." width="500" height="281" color="#f1e4be" %}

When building our privacy-first [Google Analytics alternative](https://simpleanalytics.com/websites?from=/), we had to figure out how to calculate different website tracking metrics ourselves. So the first thing we did was check out how the biggest website data devouring machine on the planet, called Google, was doing it.

## How Google calculates _time on page_

Google uses timestamps between ‘hits’ to calculate a visitor’s time on a specific page.

This means that a timer starts if a visitor lands on a page on your website. The timer clocks if the visitor navigates to another page on your website.

The timer calculates the time between the two actions as _time on page_.

What's fishy about this?

1. Google Analytics does not record the _time on page_ if you only visit one page.
2. Google Analytics does not record the _time on page_ of the last page visited.

Let's deconstruct the above statements:

1. If a visitor only visits one page and navigates away after, the timer starts but never clocks... because the visitor is not visiting a second page. The visitor is identified as a bounce. Google Analytics does not count the _time on page_ when a visitor bounces.
2. This also happens when a visitor lands on the last page. The timer starts but never clocks... because, again, the visitor navigates away and is not visiting another page on your website, so there won't be another 'hit'.

Lastly (and this is by far the most impactful one)...

Google Analytics does record the _time on page_, even if a visitor is not actively spending time on your page.

{% include gif.html slug="michael-scott-what" alt="What?" width="480" height="400" color="#473d46" %}

Let's unravel this:

You are probably familiar with the cluttered tabs like the one below.

![](https://assets.simpleanalytics.com/blog/you-are-getting-fooled-by-google-analytics-time-on-page-metric/tabclutter.png)

According to Google Analytics, I am spending time on all of these pages right now.

Every time I navigate to a different tab, the timer starts... but only clocks when I close the tab. As the tabs are still open, the timer is still recording.

Assume a visitor opened a blog post on your website but got distracted halfway and left the tab open to finish it later. According to Google, the visitor is still spending on your website and clocks the _time on page_ at 30 minutes (this is the maximum Google records).

### Here is what happens (stay with me on this one):

![](https://docs.simpleanalytics.com/images/time-on-page-ga.png)

The first screen in the illustration above shows a visit to a page on your website for 5 seconds. Let's call it page1. The visitor then navigates away to another website in a different tab for 20 seconds (in the second screen). After which, the visitor closes the tab of the other website to come back to page1 (in the third screen). After spending another 10 seconds on page 1 again, the visitor navigates to another page on your website (page2) on the fourth screen, before closing their browser.

The Google Analytics' timer starts when the visitor visits page1 of your website (+5 seconds). The timer does not stop when the visitor navigates away to the other website in a different tab (+20 seconds). When the visitor comes back to page1 on your website, the timer adds another +10 seconds before clocking at the moment the visitor visits page2. Lastly, the timer fails to record the time you spend on page2 because this is the last page the visitor visits before closing their browser.

{% include gif.html slug="math" alt="Math..." width="350" height="148" color="#ba7b4b" %}

In this situation, Google only knows the _time on page_ for the first page, not for the second.

According to Google Analytics, the _time on page_ for page1 is 35 seconds (5+20+10).

This is flawed, to say the least.

### Here is what should happen:

![](https://docs.simpleanalytics.com/images/time-on-page-sa.png)

At Simple Analytics, we figured out how to detect when a user opens a new tab and navigates to a different website. We clock our timer the moment a user moves away from the page. We can accurately measure how long a user spends on every page.

In the above illustration, the _time on page_ for page1 is 15 seconds, and for page2 it is 5 seconds — nothing more, nothing less.

In comparison to Google Analytics, we record _time on page_ when a visitor only visits one page. However, we exclude visitors who spend less than 5 seconds to provide the best insights. We consider this a bounced visitor.

## Means vs median

The data showing up in your Google Analytics dashboard measures the average _time on page_ of all your website pages. Google calculates this by using the mean. At Simple Analytics, we use the median to leave out outliers.

Consider the following example:

| Page view #                 | 1   | 2   | 3   | 4   | 5    |
| --------------------------- | --- | --- | --- | --- | ---- |
| _Time on page_ (in seconds) | 10  | 20  | 15  | 10  | 1000 |

When you calculate the average _time on page_ by using the mean, you sum up all the numbers and divide by the total number of pages. The average _time on page_ is 211 seconds.

Using the median, you account for the outlier by sorting the numbers and picking the middle number. The average _time on page_ is 15 seconds.

We feel that Google’s time on page metric is flawed, and we make a case for a better alternative. If you feel the same, give us a try. You'll be supporting an indie team of two (me & Iron) who built a privacy-first alternative to Google Analytics.

Have any questions? Ask away!

{% include gif.html slug="t-hanks" alt="Thanks from Tom Thanks..."  width="480" height="270" align="left" color="#584237" %}
