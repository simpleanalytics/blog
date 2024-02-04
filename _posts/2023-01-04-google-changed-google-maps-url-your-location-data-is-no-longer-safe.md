---
title: "Google changed Google Maps URL: Your location data is no longer safe"
author_slug: ankit
author: Ankit
excerpt: "Your location data is no longer safe as Google Maps URL changed from being a sub-domain to sub-directory"
image: https://assets.simpleanalytics.com/blog/2022-google-changed-google-maps-url-your-location-data-is-no-longer-safe/social-image-google-changed-google-maps-url.png
image_no_text: https://assets.simpleanalytics.com/blog/2022-google-changed-google-maps-url-your-location-data-is-no-longer-safe/social-image-google-changed-google-maps-url.png
related_posts:
  - /blog/why-its-time-to-move-away-from-google-analytics
  - /blog/website-analytics-without-cookies
  - /blog/is-google-analytics-illegal-in-europe
  - blog/is-google-analytics-4-gdpr-compliant
---

Google silently changed the Google Maps URL, and no one has noticed how easily they made you pass your location data to many other Google properties.

So what’s the change?

The Google Maps URL changed from `https://maps.google.com` to `https://www.google.com/maps`. This change by Google doesn’t look like a significant change at first, but if you look deeper - it is a big change.

{% include gif.html slug="big" alt="big" width="480" height="358" color="#4d4033" %}

{{tableofcontents}}

Let’s dive in!

## How do browser permissions work?

To understand what’s happening here and its impact on your privacy, let’s first outline how these browser permissions work.

Website visitors are asked for permission to share personal information all the time. In most cases, to enhance your user experience. Whenever you permit a site, say, location permission, in this case; the permission is shared across all sub-pages and directories.

**See this example to get more clarity.**

Assume you gave `https://www.example.com/some-page` your location permission. Now this means that all the pages of this website, like `https://www.example.com/other-page-1` and `https://www.example.com/other-page-2`, will have your location access, and you have given your location permission to every page on `https://www.example.com/*`.

Makes sense, right?

But the thing to remember is that webpages on `https://tool.example.com/*` or `https://widget.example.com/*` won’t have your location permission. This is because the browser treats every sub-domain like “www,” “maps,” “app,” etc., as a separate web property.

## How does this change affect your privacy?

With the above understanding, we move to Google’s latest change: The Google Maps URL changed from `https://maps.google.com` to `https://www.google.com/maps`. Google moved Google Maps from a sub-domain to a sub-directory.

This means that [Google.com](http://google.com) (their search engine) and all other properties on this domain will have your location data.

A big threat to your privacy!

This also hints that Google may move other services like Google Drive, Calendar, and Meet to a sub-directory. Hence give Google permission to access your clipboard and camera.

Think of it this way - you had to use Google Meet for a meeting, but if you give camera and microphone access to Meet, now, [Google.com](http://google.com) would have access to your camera and microphone.

## What can you do to stop this?

To be honest, you can’t do much.

However you can certainly stop using all Google services, but there will be times when you’d need to access a document hosted on Google Drive or have to attend a meeting via Google Meet.

To bypass this, you can either open these Google Meet and Drive links in incognito mode or instantly remove the permission when you are done using it.

[Here](https://support.mozilla.org/en-US/kb/site-permissions-panel) is how to do that on Firefox.

Using a different browser, you can simply search for **“Remove website permissions BrowserName.”**

## Final Thoughts

This is undoubtedly a clever move by Google to breach your privacy with little effort. Big Co. like Google are always hungry for your data and will do everything they can to get it.

A new era where your privacy is always at risk. Practices like these to get to your data are nothing new and aren’t stopped easily as Google is one of the most influential companies on earth that many rely on.

Four years ago, we took a stance against Google and built a privacy-friendly Google Analytics alternative called [Simple Analytics](https://www.simpleanalytics.com/). We believe in data privacy and an independent internet that is friendly to website visitors. If this resonates with you, feel free to have a look at[](https://simpleanalytics.com/simpleanalytics.com)

> This article is a guest blog by [Ankit](https://twitter.com/Growthfyi) from [Growthfyi.com](https://www.growthfyi.com/)
