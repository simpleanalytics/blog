---
title: Behind the scenes of building the iOS app
author_slug: onur
badge: "Guest post"
author: Onur Genes
image: /images/2021/ios-app-widgets.png
---

_We asked Onur Genes, who developed our iOS app, to write down the process. He is an experienced iOS developer who knows very well what is doable and what is not. We highly recommend him._

_Take the stage Onur!_

<img class="border-radius" src="/images/2021/onur-genes.jpg" alt="Onur Genes" />

Let me just make a quick introduction to me and my company [epist.io](https://epist.io/) first.

I am a mobile developer for a long time. I started with Android then moved to iOS. I spent more than 7 years developing mobile apps. I haven’t touched web technologies for 7 years because it was too ugly for me. That changes and these days I enjoy being a SaaS developer and heavy user of web technologies like [Next.js](https://nextjs.org/), [Express](https://expressjs.com/), [Node.js](https://nodejs.org/), [NuxtJS](https://nuxtjs.org/), etc.

When I started this blog and started to think about analytics. It is an obsession. You just want to check it all the time. “How many people are looking at my website? Where did they come from?” And it begins to evolve into an addiction.

At some point I realized I was just invading my visitors' privacy. I am a privacy activist at heart. That made me write [Being a Privacy Activist as a Developer](https://devgenes.com/posts/Being-a-Privacy-Activist-as-a-Developer/).

<img class="border-radius" src="/images/2021/ios-app-dashboard.jpg" alt="Simple Analytics iOS dashboard" />

## How did I learn about Simple Analytics?

A few years ago when I was wandering on the internet I came across [Adriaan van Rossum](https://twitter.com/AdriaanvRossum). He was talking about a product that is a competitor to Google Analytics. That seemed interesting! Being a competitor with a well-known and accepted product is a good challenge to have.

I started following him. I wasn’t a heavy user at that time but checked upon his project from time to time.

## Why being so enthusiastic about Simple Analytics?

When starting the that new blog I remembered Adriaan and his product. It was a good opportunity to use it. But back in that day, I was a student and it was hard to pay for a service. It is great but you know, you are just trying to survive as a student.

One day, I pulled the trigger. At that moment I realized I missed out on so many good things.

If you are using Simple Analytics;

1.  You don't need any cookie banners etc.
2.  It is much more useful than other analytics tools
3.  If you are paying for something, you are not giving away your privacy.
4.  It is awesome!

Time has past and I thought, it might be good to just wave a hand and say, _"Hey Adriaan, I am enjoying your product. Thanks for making this!"_ but I thought just creating an iOS app might be cooler.

<img class="border-radius" src="/images/2021/ios-app-settings.jpg" alt="Simple Analytics iOS settings" />

I contacted Adriaan and said, _“Hey Adriaan, I want to create an iOS app for Simple Analytics. What do you think?”._ In a minute he replied, _“Yes, let’s talk about that.”_

## Why did Simple Analytics need an app?

I know, not every business or every person in the world needs an app. Most of them don’t. When I only did mobile app development I was thinking like, _“I should build an app for every breathing creature in the world”_ but most of the time that's not necessary.

But companies and products like Simple Analytics need an app. Simple Analytics is using graphs heavily by its nature. Everyone using this product is looking for graphs and metrics. This is the whole point of this product. If you can show the graphs easier, it means its users will be happier.

As a user, I didn’t want to go to the website and click on the graph every time. A simple app might be more useful (and it is). With iOS 14 Apple introduced so-called _Widgets_. If I could use these technologies, I might provide value.

<img class="border-radius" src="/images/2021/ios-app-widgets.png" alt="Simple Analytics iOS showing widgets" />

## Which technologies and why?

For using widgets, you have to use [SwiftUI](https://developer.apple.com/xcode/swiftui/). It was the brand new surprise of Apple. I was making toy projects with SwiftUI but I didn’t make any serious projects. This might be the right time, so I started working on it.

In a week, we had a working prototype. It wasn't that beautiful or useful but it was working. After a few calls with Adriaan, I managed to polish it. Right now you can [download it from App Store](https://docs.simpleanalytics.com/ios-app) and use it as much as you want! It is free, and believe me, it is not tracking you!

## What is next?

After seeing the positive comments about the iOS App I decided to make an Android version as well. I will try to do my best. I am sure both apps will grow together nicely. Just [keep an eye on my tweets](https://twitter.com/onurgenes) and [Adriaan](https://twitter.com/AdriaanvRossum) for any updates.

## How can I help you and your company?

If you need an app or help with any project, [me](https://onurgenes.com/) and [my one-man company](https://epist.io/) can help you.

Thank you, Adriaan for giving me this opportunity, and thank you for reading.
