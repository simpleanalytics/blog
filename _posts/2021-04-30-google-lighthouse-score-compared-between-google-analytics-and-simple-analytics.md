---
title: Using Google Analytics can hurt your page ranking up to 9.3%
author_slug: adriaan
author: Adriaan van Rossum
badge: "Nerd post"
# image: /images/2021/ios-app-widgets.png
---

Google is adding a page experience update to their search result ranking. [They recently announced](https://developers.google.com/search/blog/2021/04/more-details-page-experience) it would roll out in mid-June and finished at the end of August. In this blog post, we will explain what that entails and that Simple Analytics has your back.

## Core Web Vitals

An important change to the Google search results will be the impact of so-called Core Web Vitals metrics. These metrics ensure a better experience for the visitor. These Core Web Vitals contain three metrics:

1. [Largest Contentful Paint (LCP)](https://web.dev/lcp/)
1. [First Input Delay (FID)](https://web.dev/fid/)
1. [Cumulative Layout Shift (CLS)](https://web.dev/cls/)

We don't go too deep into these metrics, but the general message is that they are all calculated within the performance score of Google Lighthouse. Lighthouse is a tool that Google created to measure the performance of a website. It gives a score to 4 categories: performance, accessibility, best practices, and SEO. The Core Web Vitals are included in this first category: the performance score. You can try it out yourself at [web.dev/measure](https://web.dev/measure/) (Google's online interface for Lighthouse). It runs on the servers of Google.

> To learn more about Core Web Vitals you should check out [Ahrefs blog post](https://ahrefs.com/blog/core-web-vitals/). It goes in depth about those three metrics.

Google will begin using page experience as part of their ranking systems beginning in mid-June 2021. However, page experience won't play its full role as part of those systems until the end of August.

## Performance impact of analytics tools

Analytics tools impact performances on websites. They usually add a script to the website that adds functionality. Logically this has a costs in terms of performance. Some analytics business care a lot about this, and others don't have that as a high priority. At Simple Analytics we care a lot about the impact of our embed script on the websites of our customers. We don't want to load big scripts into the browser of our customers. Although this all sounds nice, we should prove it to you as well.

[Olav Pekeberg](https://twitter.com/pekeberg_com/status/1387804377545650177) compared his website with and without Google Analytics. He found that he got a performance score whent from 93 (with GA) to 100 (without GA). The score goes from 1 to 100, and the higher, the better. He asked us how Simple Analytics was performing comparing to Google Analytics. We should perform better based on all the actions we took, but where triggered to proof ourselves.

We started with running a few tests on our computer, but the results always varied. We couldn't get a consistent result. This could have been because the internet connection, or other factors we don't know about. Then we did run it [Google's online interface](https://web.dev/measure/) for Lighthouse. Every time we did run the test it showed us a different result. As we wanted to know if we performed better we needed to run it a lot.

Luckily [Dan Sloan](https://twitter.com/Lucid_Dan/status/1387998872400666627) suggested that we run Lighthouse on a fresh VPS using the command line tool and run it a few times, grab the data via JSON, then compare without SA. That will give you the best sample set without other interfering factors.

## Test with basic page

We followed Dan's advise and created [a little Node.js script](https://github.com/simpleanalytics/lighthouse-test) around [lighthouse](https://github.com/GoogleChrome/lighthouse). We did run the test 500 times to get a trustworthy average.

- Installed the latest Google Analytics script
- Used the latest Simple Analytics script

The test tool ran around 2 hours to complete because every test did run synchronously. We didn't want to run them in parallel as this could interfere with the test results.

| Type       | Tool             | Performance score | Times | Tester           |
| :--------- | :--------------- | :---------------- | :---- | :--------------- |
| Lighthouse | None             | 95.5 (0%)         | 500   | Simple Analytics |
| Lighthouse | Simple Analytics | 95.5 (0%)         | 500   | Simple Analytics |
| Lighthouse | Google Analytics | 93.8 (-1.7%)      | 500   | Simple Analytics |

As you can see, we don't impact the performance score with Simple Analytics. But don't take our word for it. We made [our test public](https://github.com/simpleanalytics/lighthouse-test), so everybody can run the test independently. Please share your results.

## Test with more complex website

[Olav Pekeberg](https://twitter.com/pekeberg_com/status/1388070063400497152) did a test that showed more extreme results. He built [plankepriser.no](https://plankepriser.no), a website to give price transparency of construction materials in the Norwegian market. The website is more complex than the website in the previous test.

He did run the tests both on Lighthouse and [Google Page Speed](https://developers.google.com/speed/pagespeed/insights/). Both systems check for the Core Web Vitals. We rerun the test because 10 can be assumed a low number. We did run the test on his website as well 100 times.

| Type       | Tool             | Performance score | Times | Tester           |
| :--------- | :--------------- | :---------------- | :---- | :--------------- |
| Lighthouse | None             | 99.4 (0%)         | 10    | Pekeberg         |
| Lighthouse | Simple Analytics | 99.9 (+0.5%)      | 10    | Pekeberg         |
| Lighthouse | Google Analytics | 97.0 (-2.4%)      | 10    | Pekeberg         |
| Page Speed | None             | 98.2 (0%)         | 10    | Pekeberg         |
| Page Speed | Simple Analytics | 98.0 (-0.2%)      | 10    | Pekeberg         |
| Page Speed | Google Analytics | 88.9 (-9.3%)      | 10    | Pekeberg         |
| Lighthouse | None             | 0 (0%)            | 100   | Simple Analytics |
| Lighthouse | Simple Analytics | 0 (0%)            | 100   | Simple Analytics |
| Lighthouse | Google Analytics | 0 (0%)            | 100   | Simple Analytics |

The public tests data is [available on his GitHub repo](https://github.com/olavp/impact-of-analytics-on-core-web-vitals#readme).

## Conclusion

As you can see in the above numbers Simple Analytics is performing better than Google Analytics. If you care about a fast website and you are still using Google Analytics, this could be a good moment to switch. Do you want to score high on SERP (Search Engine Results Page), then it could have impact, but it's unkown how much. They write on [their blog post](https://developers.google.com/search/blog/2021/04/more-details-page-experience#gradual-rollout):

> ..., while this update is designed to highlight pages that offer great user experiences, page experience remains one of many factors our systems take into account. Given this, sites generally should not expect drastic changes. In addition, because we're doing this as a gradual rollout, we will be able to monitor for any unexpected or unintended issues.

If you want to check your website performance reguraly you can check out [Moz Performance Metrics](https://moz.com/blog/performance-metrics-beta). It's currenly in beta, but they seem to be the right tool for the job. They also [have a view](https://moz.com/blog/core-web-vitals) on the impact of search results by the Core Web Vitals performance:

> ... It's going to affect all regular search results, mobile and desktop, based on certain criteria. But also, and this is an important point, Core Web Vitals are going to become a criteria to appear in Google Top Stories. These are the news results that usually appear at the top of search results.

If you have a news site and didn't use AMP before, it might be extra important to you.

## Run your own test

To know if your website is slowing down by Google Analytics, try to run a few tests with [web.dev/measure](https://web.dev/measure/). Create a page where you run Google Analytics and create a copy of that page where you don't run Google Analytics.

Are you a developer? [Clone our repo](https://github.com/simpleanalytics/lighthouse-test) to run your own tests.

## How we stay so fast

In the recent years we have been improving our embed script a lot. Every few months if we found something that could run better or faster, we would add it. We added very optimized minimalisation of the code, we added Brotli (and of course gzip) compression, we load our script asynchronously (loads the content of the page first), we replaced our unload function with the async Beacon API (no waiting when navigating), and made sure to keep it small in size.

We are planning on keeping Simple Analytics as fast and well performing as now, and raise the bar every time.

## Useful resources

- [Google's first announcement of page experience](https://developers.google.com/search/blog/2020/05/evaluating-page-experience)
- [Google's announcement of rollout](https://developers.google.com/search/blog/2021/04/more-details-page-experience)
