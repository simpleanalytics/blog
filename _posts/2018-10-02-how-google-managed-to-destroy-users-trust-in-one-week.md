---
title: How Google managed to destroy users' trust in one week
author_slug: mike
author: Mike Timofiiv
---

This past September marks the 10-year anniversary of Google Chrome. Ever since it was released, it has changed the internet forever – its clean design, fast rendering engine and fantastic developer tools helped it acquire 62% of desktop users within 2 years. It's even more remarkable to note that the engine Chrome uses under the hood (known as V8), is used in a multitude of other ways as well, powering backend web servers through Node.js, "headless" browsing (such as by a web scraper or an automated website screenshot tool), and much more.

<img loading="lazy" src="/images/chrome-69.jpg" alt="">

There's no question it's a fantastic product. However lately, Google has seemingly broken the fourth wall in the illusion of Chrome as a benign entity. One thing Donald Trump's campaign has contributed to the world (however unintentionally) is bring up the topic of online privacy, and the climate within which the FAANG (Facebook, Amazon, Apple, Netflix, Google) giants have operated for years is beginning to change.

While Facebook was directly placed under the microscope, other companies have been caught trying to sell their influence over their users. Google is no exception, and the reach of its tentacles have become more and more of a talking point. Which brings me back to Chrome – in the latest version released 10 years after the first, a new feature was baked in called "Chrome sign-in".

The feature does something incredibly simple: it connects the identity you use in the browser application (to sync bookmarks and tabs for example) with your Google account, used to log into Google's services like Gmail, Calendar, Docs, etc. Perhaps in a different time, the feature would have received a great reception and no one would've complained, but in the last few weeks, Google's Chrome team has taken a lot of flak from annoyed and disillusioned users and the technology media. A lot of this chaos actually stems from the poor communication about the sign-in feature, as it was not written in the release notes, nor was there any kind of official announcement of such a wide-ranging change.

You might be thinking, "who cares, this just seems like no big deal to me." Well, the fact is, it is a big deal, and I'm going to explain why.

1. Google's cookies are separate from normal cookies. Meaning that once you sign in with Google in either a Google service or through your Chrome browser, their stored credentials and identifiers are exempt from you clearing your cookies.
2. It could not be turned off (this actually is going to be changed). But the original intent was that outside of a flaky developer setting in the browser (known as a flag), you would not be able to turn it off.
3. A website is a sandbox, a browser is less so. Websites cannot spy on your usage of other websites (unless through an exploit). So if you're watching porn and your Facebook is open in another tab, Facebook cannot access your porn tab. But a browser could. And for all you know, the intention is to send that usage data back to Google.

<p class="t-a-c">
<a href="https://twitter.com/ctavan/status/1044282084020441088" target="_blank" class="tweet"><img loading="lazy" src="/images/chrome-cookies-tweet.png" alt=""></a>
</p>

The worst part, however, is that scores of users will continue to use Chrome, completely unaware of the implications of this feature. Other companies, jealously eyeing Google's breach of the browser/webpage wall, will consider building similar anti-features into their browsers. That's the most insidious element of it: it pushes users' expectations and companies' freedom to breach into your privacy just one step further. The war against constant active data harvesting is not lost in one big Waterloo battle, but by many small compromises and "improvements".

A government's privilege to spy on you should begin only with a warrant issued by a court of law. This can be done if a given user is suspected of being a danger to society as a whole, such as with people that prey on children. But a private company has very limited restraints imposed on it. We say "well, Google needs to make money too" and bury our heads in the sand as if the business of systematically collecting a massive amount of data points and using them to build profiles on every individual with access to the internet for the purpose of showing them a more relevant advertisement is somehow justified by profit.

Privacy laws have made a lot of headway, like the European Union's recent [GDPR](https://eugdpr.org/) (_General Data Protection Regulation_) and Canada's [_Fighting Internet and Wireless Spam Act_](https://en.wikipedia.org/wiki/Fighting_Internet_and_Wireless_Spam_Act) (also known as CASL – _Canada's Anti-Spam Legislation_: technically an anti-spam legislation, but it contains a set of rules about consent), but unfortunately legislation and innovation are the nuclear arms in the war between legislators and big tech. As consumers and citizens we should all take time to let our governments know how best to govern these big entities.

But there is one thing we can all do as individuals as well, something that doesn't require voting or calling your senator or member of parliament. You can simply choose to **not** feed the beast, as much as you can. Install a different browser to replace Chrome such as [Firefox](https://www.mozilla.org/en-US/firefox/new/), [Ungoogled (Eloston) Chromium](https://github.com/Eloston/ungoogled-chromium), [Vivaldi](https://vivaldi.com/) or [Brave](https://brave.com/). Switch email providers from Gmail or Outlook to Protonmail. Install a VPN such as ExpressVPN. Replace your bloatware Android OS on your phone with something like [Lineage OS](https://lineageos.org/).

And if you're a maker, employee in a company with a website or digital product, own a blog, or in any other way need to track visitors, do the ethical thing and stop feeding Google your users' data and use something like [Simple Analytics](https://simpleanalytics.com/?ref={{ site.hostname }}).
