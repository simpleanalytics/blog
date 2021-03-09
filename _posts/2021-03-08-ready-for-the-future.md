---
title: Ready for the future and hit $100k ARR
author_slug: adriaan
badge: "Company update"
author: Adriaan van Rossum
image: /images/2021-03/100k-mrr.png
---

In the last months, we have been working hard to get ready for the future. At the same time, we hit our $100k ARR milestone! We are very happy with the features that are only possible because of all the groundwork we did. In this post, we share some extra numbers around our milestone and dig into our newly developed features of the last months.

### New data structure for new features

We developed our database structure from the ground up and build on top of the fantastic work of Elastic. We are very grateful that we can use their open-source software to grow our business to the next level. In this update I will walk you through all the updates we added to Simple Analytics and some background information on the choices we made.

<details markdown="1">
<summary>Node.js example to show the top 10 UTM sources for Hacker News in Elasticsearch</summary>

```js
const { Client } = require("@elastic/elasticsearch");
const client = new Client({ node: "http://localhost:9200" });

const {
  body: { hits },
} = await client.search({
  index: "pageviews-*",
  body: {
    query: { term: { hostname: "news.ycombinator.com" } },
    aggs: {
      top_10_utm_sources: {
        terms: { field: "utm_source", size: 10 },
      },
    },
  },
});

console.log(hits);
```

</details>

At the time we launched the first version of Simple Analytics back in 2018 we wanted to build the prototype as fast as possible. That required us to use the tools we were familiar with and that included the database. Because of that we picked PostgreSQL (a very common database) and stored all page views in it. It worked super nice and as we grew we added caching tables with aggregated data. This required us to update the database schema and caching tables as we build new features. Not ideal if you want to rapidly iterate on your product.

### Filtering data

One of the most requested features was being able to filter on certain data points. If you would like to know which pages are popular in Germany you would expect to click on Germany and see all the other data update with Germany filtered. To make this possible within our previous database solution it would request much more work and way more error-prone.

{% include video.html slug="filters" %}

### APIs

Because we use our new database system for our APIs as well, it has been largely expanded. As a customer, you can get all the data you see in our dashboard. We see a lot of customers using it for amazing use cases.

<ul>
  <li><a href="https://nomadlist.com?utm_source=blog.simpleanalytics.com">Nomad List</a> uses the Simple Analytics data to calculate the price of their ads on certain pages.
  </li>
  <li>
    <p class="mt-0 mb-05"><a href="https://chartbrew.com/?utm_source=blog.simpleanalytics.com">Chartbrew</a> can make fancy charts based on Simple Analytics data.</p>
    <a href="https://app.chartbrew.com/b/Simple_Analytics_296">
      {% include video.html noLink="true" slug="chartbrew" %}
    </a>
    <p class="caption mt-0"><a href="https://app.chartbrew.com/b/Simple_Analytics_296">A public demo</a> of our data on <a href="https://chartbrew.com/?utm_source=blog.simpleanalytics.com">Chartbrew</a></p>
  </li>
  <li>Niklas Metje created an <a href="https://niklasmtj.de/blog/simple-analytics-ios-widget-with-scriptable">iOS widget with Scriptable app</a></li>
</ul>

There are many more customers who API internally but we can't show that obviously.

> [See our documentation](https://docs.simpleanalytics.com/api) to learn about our APIs

### $100k milestone

While writing this blog post we hit a nice milestone for our business. We hit $100k ARR (Annual Recurring Revenue). For us, it feels like a big thank you from all our customers. All the new features were not possible without all the customers that already believed in our product in the early stage.

<img class="border-radius" style="width: 544px" src="/images/2021-03/100k-mrr.png" alt="100k ARR poster" />

### Time on page

In the last month, we added time on the page to our dashboard. As we usually build things from the ground up we think about how to make our numbers better than what customers would see at competitors. We don't want our customers to think that their website is doing great with huge numbers instead of what is actually happening. Time on page is a great example of that.

For example, Google Analytics does show time on site and time on page metrics on their dashboard. This metric is being used as the **actual** time on page by most people. We will clarify this in a later blog post. In short Google Analytics uses averages for data points that have quite some outliers. In mathematics, this is considered bad practice. We use the median to get the time on page. Google Analytics also calculates the time when a page is in the background. One of the reasons why their time on page is way too high (they do limit it to sessions length which is 30 minutes by default).

{% include video.html slug="time-on-page" %}

It has its advantages to build new features without looking too much to the competition first. Instead of just copy-pasting, we try to really think about those numbers and methods and find the best ones for our customers.

### Social images

Because getting data out of our API it's easier for us to develop new features. One of the features that we wanted to build for a long time were the social media images. Because we offer the option to make a dashboard public you are encouraged to share your statistics. To make that experience more awesome we decided to integrate the chart into it. Here is an example for [oneweektomake.com](https://oneweektomake.com/?utm_source=blog.simpleanalytics.com).

<p class="mb-0"><a class="mb-0" href="https://twitter.com/pooria_r/status/1361071130736422912"><img class="border mb-0 mt-0" style="width: 544px" src="/images/2021-03/social-images.png" alt="Tweet with social image of Simple Analytics feature" /></a></p>

<p class="caption mt-05 ta-c">The Simple Analytics social image feature <a href="https://twitter.com/pooria_r/status/1361071130736422912">in Pooria Rashidi's tweet</a> (<a href="https://twitter.com/SimpleAnalytic/status/1350803898622242823">source code</a>)</p>

### Transparency

As a transparent startup we care about sharing our insights with you. We updated our [open page again](https://simpleanalytics.com/open) with new data for last month.

Thanks for reading and please ask any questions if you have some. We love to make this interesting for everybody. Have a good one!
