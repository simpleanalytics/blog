---
title: Why FLoC is a FLoP
author_slug: tim
author: Tim de Nood
image: /images/2021-05/am-i-floced.png
excerpt: Google says FLoC is "a privacy-preserving mechanism for interest-based ad selection." We beg to differ. Here's how to stop Google from selling your data to advertisers (again).
---

Here's how to stop Google from selling your data to advertisers (again).

I have to admit that I first thought that Google was finally taking some steps towards a privacy-friendly web with FLoC. Until I started researching.

_Will we tolerate Google transforming individual surveillance into mass surveillance without giving people a real choice? And let them frame this act as "privacy-preserving"?_

# What is FLoC?

Federated Learning of Cohorts, or FLoC for short, was invented because Google recognizes the privacy problems of third-party cookies. However, **they still want to let advertisers target you based on what you do on the web**. With Apple launching a privacy report in Safari, Google jumped on the bus to restrict third-party cookies in Chrome. Yet, replacing them with a brand new tracking technology is not the answer.

Google says FLoC is "a privacy-preserving mechanism for interest-based ad selection."

It is designed to aid advertisers in performing behavioral targeting without the need for third-party cookies by collecting information about people's browsing habits. Google will use this information to create certain "_cohorts_," where they will put people with similar interests and browsing patterns into the same specific group.

**Google will give every browser an ID based on these patterns** to indicate which groups they belong to - so advertisers can use them for mass targeting that is supposed to be "anonymous."

On their [blog](https://blog.google/products/chrome/privacy-sustainability-and-the-importance-of-and/), Google says that the initial testing of FLoC is already taking place. They're testing it on users in Australia, Brazil, Canada, India, Indonesia, Japan, Mexico, New Zealand, the Philippines, and the U.S. They will branch out to other regions as the trial expands globally. **Only people who've chosen to block third-party cookies in Chrome will be excluded automatically**. _(Btw, you can test if you're already "FloCed" by Google on [amifloced.org](https://amifloced.org/))_

This means Google is again forcing people to participate in their profit-making experiment because we've already seen that **most people do NOT choose to opt-out themselves** for cookies.

All of the above raises essential questions and privacy issues, and we haven't even gone below the surface level of FloC.

Let's uncover the hidden parts of this new machine, explore what's happening below the hood, and you'll see why FLoC a forceful privacy FLoP:

# The "Good"

As you've seen in the previous section, the main goal is to preserve people's privacy. That is a good thing. Luckily, more and more people are becoming privacy-aware. Here at Simple Analytics, we see that the most popular reason for ditching Google Analytics to our fast, simple, and privacy-first analytics is ethics. We do not store users' information. We don't chase you with ads. We don't track you. **Never**.

Another excellent example of the movement towards privacy is DuckDuckGo, a privacy-focused search engine that never tracks people. And there are much more privacy-friendly alternatives being developed to combat the enormous online power of Google.

<img loading="lazy" class="border" src="/images/2021-05/duckduckgo.png" alt="DuckDuckGo" />
<p class="caption">The privacy-friendly search engine <a href="https://duckduckgo.com">DuckDuckGo</a>.</p>

While we as innovators are fighting together for privacy, users make more conscious choices about the apps they use. Google also noticed this shift and immediately started to work on a "solution." Google also decided to battle privacy-invasive cookies. Good news? Not really.

Although Google decided to throw cookies out, **that doesn't mean its privacy-invasive methods are _gone_.** Just like with a pot of water, you choose to boil. It doesn't disappear; it simply changes form. It turns into steam, or you could say: **It becomes invisible**.

According to Google, FLoC was designed to - and is supposed to - do less harm. But is that so?

While FLoC is indeed made to prevent a particular threat - individualized tracking and information collecting - **it does not guarantee that our privacy will remain intact.**

You are, as the rest of this article will show, _still being followed._

Before we show the rest of the unethical details of FLoC (and in case you don't want to read everything), **here is a quick way to prevent "being FLoCed":**

## How to escape the privacy-invading tactics from Google as a user?

Luckily, we **_can_** escape. The most effective method to stop Google from selling your data is to **stop using Google Chrome and other Google-related products.** Banning Google from your life as much as you can, is most likely to protect you from future privacy invasion. Though it might not seem feasible at first, the degree of security and protection you gain back with that decision far exceeds the value of comfort that comes at the cost of leaving all of your data exposed.

There is also a second-best option to opting out. Here's how:

- Log out of your Google account and [turn sync history data off](https://support.google.com/chrome/answer/185277?co=GENIE.Platform%3DAndroid&hl=en) with Chrome
- Block third-party cookies or browse only in incognito mode
- Disable these in Google Activity Controls: "Web & App Activity," "Include Chrome history and activity from sites, apps, and devices that use Google services."
- Disable these in your Google Ad Settings: "Ad Personalization," "Also use your activity & information from Google services to personalize ads on websites and apps that partner with Google to show ads."

How to block third-party cookies and opt-out of FLoC:

{% include video.html slug="opt-out-of-floc" %}

As a web user, your only way out of this is to make a conscious decision to no longer take part in this exploitation. With the way the internet is organized, **it is up to you.** It will probably take a long time before governments start to penalize privacy-invasive behaviors. Therefore, **we should take matters into our own hands and make conscious decisions to protect our privacy.**

We know that Google doesn't make it easy, and that's the problem. The most ethical solution would be that you had to **_opt in_** to be tracked. Unfortunately, Google knows this wouldn't be the most profitable solution for them.

Most people are likely not going to bother to look up how to disable FLoC, and Google is very aware of our natural tendency to choose comfort.

### Opt-out as a website owner

If you are a website owner, **your site will _automatically_ be included in FLoC calculations** if it has access to the FLoC API or if Chrome [detects that it serves ads](https://chromium.googlesource.com/chromium/src/+/master/docs/ad_tagging.md).

Luckily, as a website owner, you can also decide to [opt-out](https://developer.chrome.com/blog/floc/#how-can-websites-opt-out-of-the-floc-computation) of the FLoC calculation by sending the following HTTP response header:

```
Permissions-Policy: interest-cohort=()
```

As we've seen, it's important that we choose to take action towards increasing our security and privacy ourselves. But what happens if we don't?

# The Bad

Let's say you leave the option on and allow Google to place you in cohorts based on your browsing habits on the web. After all, "it's safer to be in an **_observed group_** than to be _individually tracked_."

The problem is that FLoC cohorts shouldn't - under any circumstances - function as identifiers on their own.

Because that way, any company would be able to use it to their advantage, for example, by giving you the option to log in with your Google account for the "simple and easy" use of their service.

**If that happens, they would be able to connect that information with your FLoC profile and instantly learn about you without the use of cookies**.

This could even include private information about your browser history, which could be traced back to the sites you may have or certainly visited.

That's not all.

<img loading="lazy" class="border" src="/images/2021-05/am-i-floced.png" alt="Am I FLoCed?" />
<p class="caption">Check if your Chrome browser is FLoCed on <a href="https://amifloced.org/">amifloced.org</a>.</p>

With the use of this technology, they could also uncover general information about your demographics and interests. Savvy advertisers could determine what kind of person belongs to specific cohorts, including their age, gender, political view, and perhaps even their skin color.

**This is - _without a doubt_ - sensitive information.** Google is invading your privacy again, but this time with a clever twist that even frames them as the heroes of the story.

Google has proposed monitoring the system and looking for any associations with sensitive categories. If it finds a particular cohort that is too closely related to a specific group, the server could choose new parameters for the algorithm and regroup those users.

This solution produces even more significant privacy issues.

To monitor how FLoC groups correlate with sensitive categories in the first place, **Google would have to collect and observe an astronomical amount of data about users' race, gender, religion, age, health, and financial status**.

This is simply unacceptable.

And it doesn't stop here.

# The Ugly

The FLoC project's Github page addresses upfront:

This API democratizes access to some information about an individual's general browsing history (and thus, general interests) to any site that opts into it. Sites that know a person's PII (e.g., when people sign in using their email address) could record and reveal their cohort. This means that information about an individual's interests may eventually become public.

This means every site you visit will have a good idea about what kind of person you are on the first contact, without having to do the work of tracking you across the web. Moreover, as your FLoC cohort will update over time, sites that can identify you in other ways will also be able to track how your browsing changes.

Remember, a FLoC cohort is nothing more, and nothing less, than a summary of your recent browsing activity.

This shows that it isn't by far a more privacy-friendly alternative. Arguably, it may be even more intrusive. Can it be different?

# Let's imagine a world without privacy invasion.

A quote on a [blog about the problems of FLoC](https://www.eff.org/deeplinks/2021/03/googles-floc-terrible-idea) by Bennett Cyphers states:

> "Instead of re-inventing the tracking wheel, we should imagine a better world without the myriad problems of targeted ads."

If FLoC becomes the new norm, it may be more difficult to target users based on their age, gender or income, but it will still be possible.

Advertisers would dive into this new world of information, research, and learn about the FLoC groups **until eventually, they would figure out what sorts of users would be placed inside certain cohorts**.

The resolute and persistent people in this new world would dominate and reap substantial rewards.

Plus, it will be even harder to regulate these kinds of behaviors.

It gives trackers a perfect excuse since they wouldn't be targeting anyone "directly" - they would stick to the rules and only use these new, "protected" cohorts as good boys. That doesn't sound like the kind of future you would agree to, right?

Fortunately, this doesn't _have_ _to_ happen. Of course, Google can still decide to abandon the idea and leave behind its obsession with surveillance. Yet, how likely do you think Google (a data company) will leave surveillance and data-gathering practices soon?

That's what we thought... That isn't going to happen. So...

**We advise you to take matters into _your own hands_ and take action on how much you want to be surveilled. Tell others to do the same. Because if you yourself don't respect your privacy, _who will?_**

Simple Analytics emphatically rejects the future of FLoC. That is not the world we want, nor the one users deserve. Google needs to learn the correct lessons from the era of third-party tracking and design its browser to work for users, not for advertisers.

If you want to stay up to date about the latest privacy news, consider subscribing to our brand-new newsletter at [ThePrivacyNewsletter.com](https://theprivacynewsletter.com).

This monthly email gives you a short and handy overview of what's going on in the online privacy world.

If you want to analyze your website and _care about your privacy and visitors' privacy_, [try Simple Analytics for FREE](https://simpleanalytics.com).

It gives you all the website insights you need in one simple and intuitive dashboard - **without** **tracking anyone.**

You can start your [free 14-day trial here](https://simpleanalytics.com). No strings attached.
