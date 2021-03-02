---
title: Ready for the future
author_slug: adriaan
badge: "Company update"
author: Adriaan van Rossum
image: /images/2020-05/woman-using-pc-and-android-phone-at-home-office.png
---

In the last months we have been working hard to get ready for the future. We are also very happy with the features that are only possible all the ground work we did. We developed our database structure up from the ground and build on top of the fantastic work of Elastic. We are very grateful that we can use their open source software to grow our business to the next level. In this update I will walk you through all the updates we added to Simple Analytics and some background information on the choices we made.

### Elastic

At the time we launched the first version of Simple Analytics back in 2018 we wanted to build the prototype as fast as possible. That required us to use the tools we were familiar with and that included the database. Because of that we picked PostgreSQL and stored all page views in it. It worked super nice and as we grew we added caching tables with aggregated data. This required us to update the database schema and caching tables as we build new features. Not ideal if you want to rapidly iterate on your product.

### Filtered data

One of the most requested features was being able to filter on certain data points. If you would like to know which pages are popular in Germany you would expect to click on Germany and see all the other data update with Germany filtered. To make this possible within our previous database solution it would request much more work and way more error prone.

### APIs

Because we use our new database system for our APIs as well, it has been large expanded. As a customer you can get all the data you see in our dashboard.

This monthly update contains 3 months in one. We will look back on the previous months and take a look in the future. For the first time we experience slower growth than normal and here we explain what we are going to do about it.

<img loading="lazy" class="border" src="/images/2020-08/01-mmr-growth@2x.png" alt="MMR growth of Simple Analytics">

---

We started doing monthly updates on Twitter with our learnings, revenue, new expenses, new features, and more. From this month on we will also share it on this blog. In this post we talk about referrer spam, abroad payments, Mindwave, badges, and password login.

<img loading="lazy" class="border" src="/images/2020-04/open-page.jpg" alt="Open page of Simple Analytics">

At the first of May we had 399, but we passed 400 customers soon after. At the first of the month we had an MRR of $5451 and an ARR of $65k. We see a bigger growth than normal. It's likely due to our product being free for corona products. In exchange, we ask for a link back to the public stats of the project.

Especially [corona-data.ch](https://corona-data.ch) ([data](https://simpleanalytics.com/simpleanalytics.com/referrers/corona-data.ch)) gave us a lot of traffic with 6.6M visitors in the last month. We also helped build a COVID-19 app: [coronastatus.nl](https://coronastatus.nl) which was started by [BustByte](https://bustbyte.no). It's now translated in many languages and available in many countries.

This corona status project we paid quite some domains. That's why our hosting bill this month is higher than normal. You can see that more clear on our [open page](https://simpleanalytics.com/open) graph.

We also ordered a new bare metal server for [Elasticsearch](https://en.wikipedia.org/wiki/Elasticsearch) which James almost has completed. We tested this with lots of test data and the Elasticsearch API is super fast. We can't wait to show you what we have done with it. Expect new features to roll out in the next couple of months.

<img loading="lazy" class="border" src="/images/2020-04/kibana.jpg" alt="">
<p class="caption">In the image you see <a href="https://en.wikipedia.org/wiki/Kibana" target="_blank">Kibana</a>, a great tool for Elasticsearch</p>

When installing our new server we didn't find a great guide on how to encrypt a server. We had some specific requirements. We decided to [write a guide](https://blog.adriaan.io/install-ubuntu-server-18-04-4-with-raid-1-encryption-grub-and-legacy-bios.html) on how to encrypt your disks on your server (it's very technical and long).

To remove spam in your analytics data we added a feature where you can just do that in a few clicks. Sometimes silly referrals pup up in your dashboard from unethical companies trying to sell their products. We created [a simple way](https://docs.simpleanalytics.com/remove-referral-spam) where you can delete those.

<img loading="lazy" class="border" src="/images/2020-04/referrer-spam.jpg" alt="Referrer spam">

We would love to explain a bit about how we deal with payments for our freelancers. It was a bit of work to figure out what was the best solution. PayPal is super expensive and others were as well. The cheapest and fastest option we found was [Transferwise](https://transferwise.com/). We can transfer $1000 for about $10 and it arrives within minutes on their account. It might be different from your country.

Last month we also paid for a yearly subscription of [Mindwave](https://mindwave.app). It's an all-in-one journal for work and life. It's made by [Marcel Hagedoorn](https://twitter.com/marcelhagedoorn) and it's a great way of logging how your days go. It has a Telegram integration which I love and asks me a question every day. You can also keep your notes in there, and that's the place where these monthly updates originate from.

<img loading="lazy" class="border" src="/images/2020-04/mindwave.jpg" alt="Mindwave">

We are very proud to have almost 400 customers. It's something we could only dream of when we started. We hope this will continue for the next coming years so we can even build better and smarter features for your data.

We also [launched our badges](https://simpleanalytics.com/badges). We took some extra time to make the badges privacy friendly. For example we added referrerpolicies ([documentation](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Referrer-Policy)) to the HTML elements, preventing data from the page to end up on our servers. Scroll down to privacy on the badges page to read more.

<img loading="lazy" class="border" src="/images/2020-04/badge-saas-for-covid.jpg" alt="Badge on saasforcovid.com">
<p class="caption">
  The badge in action on <a href="https://saasforcovid.com" target="_blank">saasforcovid.com</a>
</p>

A lot of customers asked us about password login. It's something we wanted to offer for a long time but never got to it. So we challenged ourselves. We promised 5 starter plans to give away when we would not finish this feature in 2 months. It was done just within that deadline, thanks for pushing us @nathfrederand and [@JustinNoelDev](https://twitter.com/JustinNoelDev)!

<a href="https://twitter.com/troyhunt/status/1226244918894448640" target="_blank">
  <img loading="lazy" class="border" style="width: 450px" src="/images/2020-04/tweet-troy-hunt.jpg" alt="Passwordless login is an absolute pain in the arse; enter an email address only but you're not logged in, you need to wait for the email to arrive. So you wait. And wait. It might be very quick, it might be delayed, it might go to junk, it might bounce... by Troy Hunt" />
</a>
<p class="caption" style="text-align: center;">
  <a href="https://twitter.com/troyhunt/status/1226244918894448640">Tweet</a>
  by Troy Hunt
</p>

We might have missed some numbers in this thread. We updated our [open page again](https://simpleanalytics.com/open) with all new data for this month. It also says we have more than 400 customers now!

<img loading="lazy" class="border" src="/images/2020-04/password-login.jpg" alt="Password login">

That's it for this month! Thanks for reading and please ask any questions if you have some. We love to make this interesting for everybody. Have a good one!
