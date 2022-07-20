---
title: "Vodafone & Deutsche Telekom to introduce persistent user tracking"
author_slug: iron
author: Iron Brands
excerpt: "Vodafone & Deutsche Telekom are trialing with Trustpid to introduce persistent user tracking"
image: https://assets.simpleanalytics.com/blog/2022-Trustpid/vodafone-deutsche-telekom-trustpid.png
image_no_text: https://assets.simpleanalyticsassets.com/blog/2022-Trustpid/vodafone-deutsche-telekom-trustpid-social-image.png
draft: true
---

Vodafone & Deutsche Telekom recently started trials with Trustpid to reintroduce persistent user tracking.

Network operators are a vital part of transmitting data traffic on the internet. In this process, the data is sent largely untouched. This is about to change as Vodafone & Deutsche Telekom are tapping into ways to monetize these data streams.

They have recently started a trial to test new ways of marketing customer data in collaboration with Trustpid.

Although Vodafone claims there is nothing to worry about, privacy officials are especially concerned about the recent involvement of network operators.

Privacy advocates call it the return of the "Super Cookie." If they are correct, this would be a massive step backward in creating an independent web where the privacy of internet users is respected.

1.  [Persistent User tracking: How does it work?](#1--persistent-user-tracking-how-does-it-work)
2.  [Why is Vodafone reinventing persistent user tracking?](#2--why-is-vodafone-reinventing-persistent-user-tracking)
3.  [How privacy-friendly is this?](#3--how-privacy-friendly-is-this)
4.  [How to avoid persistent user tracking?](#4--how-to-avoid-persistent-user-tracking)

{% include gif.html slug="spy" alt="spy" width="500" height="500" color="#7e7148" %}

Let's dig in! 

## 1.  Persistent User tracking: How does it work?

It's supposed to work like this: Your activity online makes your device send an HTTP request. Network operators like Verizon or Vodafone facilitate the data transmitted by this request. Until now, these network operators did not interfere in the transmission and merely forwarded the data.

Verizon was the first provider to interfere with this data traffic by injecting an HTTP header (basically an identifier), and now Vodafone and Deutsche Telekom are testing something similar.

<img src="https://assets.simpleanalytics.com/blog/2022-Trustpid/vodafone-deutsche-telekom-trustpid.png" alt="trustpid super cookie" class="border-radius" />
<p class="caption" markdown="1">
</p>

With TrustPid, Vodafone assigns a fixed ID to a user based on someone's phone number.

Through an API, website operators would then be able to call up this identifier to exactly see what websites this user has visited and create a profile to display targeted ads. 

## 2.  Why is Vodafone reinventing persistent user tracking?

Well, the internet runs on advertising. It's a multi-billion dollar industry that relies on mass surveillance. In recent years the playing field for user tracking has changed a lot for the better (although this depends through what lens you look at it).

GDPR is finally showing its teeth, and consumers demand more privacy. This has led to changes primarily driven by privacy concerns:

-   Many web browsers block third-party cookies, and even [Google Chrome is phasing out third-party cookies](https://www.theverge.com/2021/6/24/22547339/google-chrome-cookiepocalypse-delayed-2023) next year.
-   Data protection agencies in EU member states have banned using Google Analytics ([CNIL, France](https://blog.simpleanalytics.com/cnil-update-google-analytics-is-still-illegal) and [DSB, Austria](https://noyb.eu/en/austrian-dsb-eu-us-data-transfers-google-analytics-illegal) and [Garante, Italy](https://blog.simpleanalytics.com/italy-declares-google-analytics-illegal)).
-   Google is [sunsetting Universal Analytics](https://blog.simpleanalytics.com/google-to-sunset-universal-analytics-in-2023) in favor of GA4.

Another big blow was [Apple cracking down on user tracking](https://blog.simpleanalytics.com/does-safari-block-google-analytics-and-apple-privacy-updates), costing Facebook billions in revenue. They recently released the App Tracking Transparency (ATT) feature that asks if users want to be tracked when they open the app. [Facebook announced](https://www.cnbc.com/2022/02/02/facebook-parent-meta-fb-q4-2021-earnings.html) that this move would cost them at least 10 billion in ad revenue.

It has become more challenging to monetize customer data, so the advertising market is looking for new solutions to tap into. They do not want to go back to non-personalized advertising, so they are pushing the frontier to see what's still possible. The Trustpid trial is an example of this.

The industry is losing the battle for third-party cookies, so they are now exploring different ways to get advertising IDs.

Vodafone not only wants to provide the advertising IDs but also manage who can access them. This way, network operators will play a central role in the advertising industry.

## 3.  How privacy-friendly is this?

In 2016, [Verizon received a fine of 1,35 million USD](https://www.theverge.com/2016/3/7/11173010/verizon-supercookie-fine-1-3-million-fcc) by the FCC for exactly doing this. Vodafone & Deutsche Telekom are doing things differently and claims the trial is privacy-friendly by design and in line with GDPR law.

In a [reaction to Wired](https://www.wired.com/story/trustpid-digital-token-supercookie/), Vodafone says that Trustpid is not a super cookie because it does not build customer profiles as Verizon did. Each partner website with access to the data generates a different token for the same user, reducing the likelihood of building a profile across multiple websites.

The Trustpid pilot is designed to be a game changer in the wake of more privacy measures that reduce the effectiveness of online advertising. According to Vodafone, Trustpid will give advertisers again the information they need while protecting personal data.

Not everyone agrees with the privacy-friendliness of this trial. Network operators are in a unique position. They can still link data traffic to a cell phone number even without cookies. This means that users can be tracked across websites, and there is not much you can do about it.

Even if these cell numbers were anonymized, a user profile could be built relatively easily if you connect all the metrics that are being collected. The anonymous identifier can be reassigned to a specific user when, for example, logging in on a website.

The fact that users are less in control raises concerns with privacy advocates. Cookie banners (unclear as they are) still put website visitors in control. In addition, network operators have always been 'just forwarders of data' and are now deliberately putting their trustworthy position at stake. 

## 4.  How to avoid persistent user tracking?

There are a few ways to avoid being tracked by the "Super Cookie." First, you can stop using Vodafone or Deutsche Telekom as your network operator. These are the only networks that are currently involved in the trial.

In addition, Apple is developing features to restrict network operators from intervening in the data traffic. This is called the ["iCloud Private Relay,"](https://www.lifewire.com/what-is-icloud-private-relay-5200343) which ensures providers no longer have access by encrypting and redirecting the data via Apple's servers. Vodafone and Deutsche Telekom have already filed a complaint to the European Commission to stop Apple from doing this.

Another solution would be to use a VPN provider. Like the iCloud Privacy Relay, it will route the traffic encrypted to that one provider. Your network operator only sees that provider, not the websites you visit via the provider. We can recommend [Proton VPN](https://protonvpn.com/) and [Mozilla VPN](https://www.mozilla.org/en-US/products/vpn/) based on their mission toward privacy. If you are a developer, you use [Algo VPN](https://github.com/trailofbits/algo), which you can install on your own server.

##  Final Thoughts

Whether you think persistent user tracking is good or bad depends on your perspective. Advertisers that are struggling to deal with privacy laws might view this as an alternative to third-party cookies.

However, at Simple Analytics, we believe this is a massive step in the wrong direction. We believe in creating an independent web that is friendly to website visitors. This is the reason why we built a [privacy-first alternative to Google Analytics](https://blog.simpleanalytics.com/why-simple-analytics-is-a-great-alternative-to-google-analytics).

There is a reason why even Google Chrome is phasing out third-party cookies in 2023. Its because consumers demand privacy.

Privacy is a human right and should be treated as one. Trialing with persistent user trackers, where the effectiveness of consent is very questionable, to say the least, does not treat privacy as such.

We don't need a "new" tracking solution that pushes the edges of what is morally acceptable. We just need to figure out how to navigate our businesses with less tracking. We need to adopt a different mindset and figure out how to become independent from those data-crunching beasts.
