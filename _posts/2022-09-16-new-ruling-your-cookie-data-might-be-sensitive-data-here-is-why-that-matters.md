---
title: "New ruling: Your cookie data might be sensitive data. Here is why that matters"
author_slug: carlo
author: Carlo Cilento
excerpt: "Cookies have always been treated as personal data under the GDPR, but are now considered sensitive data under the new ruling"
image: https://assets.simpleanalytics.com/blog/2022-your-cookie-data-might-be-sensitive-data/social-image.png
image_no_text: https://assets.simpleanalytics.com/blog/2022-your-cookie-data-might-be-sensitive-data/social-image-no-text.png
draft: true
---

In a [recent case](https://gdprhub.eu/index.php?title=CJEU_-_C%E2%80%91184/20_-_Vyriausioji_Tarnybin%C4%97s_Etikos_Komisija), the EU Court of Justice ruled that 'data' which can reveal 'sensitive data' should be regarded as 'sensitive data.'

Upon this point, cookie data has always been treated as personal data under the GDPR and not as sensitive data. But what if cookies were actually considered sensitive data in light of this judgment? What would the implications be?

In this article, we outline why this scenario is not far-fetched and why it would deeply impact how we use cookies.

{% include gif.html slug="explain-like-five" alt="explain like five" width="480" height="400" color="#574840" %}

1.  What is the case about? 
2.  What does the ruling mean?
3.  The practical implications
4.  What does it mean for cookies?

## 1. What is the case about?

The case at hand was brought by the director of a Lithuanian establishment that received public funding. Under Lithuanian law on conflict of interest, he was required to provide certain personal information- including the name of his spouse - to an Ethics Commission for publication.

The director refused to provide the information. He claimed that disclosing his partner's name on a publicly accessible website would indirectly disclose his sexual orientation, which constitutes sensitive data under the GDPR. [^footnote]

He brought his case to an administrative court and later landed in the EU Court of Justice for a preliminary ruling. The Court finally ruled that data from which sensitive data can be deducted should themselves be treated as sensitive data under the GDPR.

## 2. What does the ruling mean?

The GDPR protects personal data in general but lays out stricter rules for particularly sensitive categories of data, such as health data, political opinions, religious beliefs, and sexual orientation. As the Court explicitly noted, a person's name is not, in and of itself, sensitive data. However, such data can reveal the person's sexual orientation, which is indeed sensitive data. For this reason, the Court held that the name of someone's partner could qualify as sensitive data.

This ruling opens a big can of worms. Lots and lots of personal data are not sensitive in and of themselves but may reveal sensitive information. 

## 3. The practical implications

The online advertising industry currently gathers enormous amounts of data to profile Internet users for personalized ads, some of which target users based on sexual orientation, health conditions, and political beliefs (or by reliable proxies of such sensitive properties).

It's hard to believe that none of the data processed for this kind of advertising is liable to reveal sensitive information. This is especially true for large, data-driven tech companies like Google or Facebook. When large amounts of personal data are combined and fed to their sophisticated, AI-driven algorithms, even apparently "neutral" information may reveal sensitive data about a user.

The impact of this ruling may not be limited to big tech companies. Let's say a website processes third-party cookies. A user's browsing habits are not sensitive data in and of themselves, but it's easy to think of examples where sensitive inferences can be drawn from them. What if the user visited informational websites about specific health conditions, online communities related to mental health, or websites hosting pornography? And what about any first-party cookies processed by those very "sensitive websites"?

Right now, it's difficult to guess how broadly the ruling will be applied in future case law. But in light of the Court's reasoning, it's hard to argue that no sensitive data would be processed in any of the above scenarios.

This also goes for the disclosure of the data to third parties: if a website processed sensitive cookie data through Google Analytics, the website and Google would be, respectively, the controller and the processor of sensitive data.

<img src="https://assets.simpleanalytics.com/blog/2022-your-cookie-data-might-be-sensitive-data/social-image-no-text.png" alt="cookie data" class="border-radius" />
<p class="caption" markdown="1">
</p>

## 4. What does it mean for cookies?

More data may be considered to be sensitive  and will be subject to stricter rules under the GDPR. In fact, some data processing operations may not be lawful anymore under the stricter regulation for sensitive data.

If cookie data - or at least some - were considered sensitive data, they would require the user's explicit consent - that is, a "reinforced" form of "baseline" consent under the GDPR. There are other ways to comply, but from a practical perspective, obtaining explicit consent from the user will be the only option in most scenarios.

This might not seem like a big deal since user consent is already mandatory for cookies under the ePrivacy Directive. However, cookie consent is collected in ways that are... not ideal, to say the least. "Cookie fatigue" is a well-known phenomenon that drives most users to accept cookie policies without even clicking them, let alone reading them. Additionally, many cookie banners use deceptive designs to make it as annoying as possible for the user to refuse consent. Given the GDPR's general requirement that consent be free and informed, these practices are problematic, to put it mildly.

If cookies- or at least cookies for certain websites- were to require explicit consent in the future, supervisory authorities may adopt a stricter stance on cookies overall and start taking the requirements for "baseline" consent more seriously. Even if authorities don't go as far as to require explicit consent, the recent judgment and the discussion it sparked might highlight the many shortcomings of cookie implementation.

## Final Thoughts

At the moment, no one can accurately assess the future impact of the ruling, as there is no guidance or other case law yet. We don't have a crystal ball, but we have good reasons to believe this ruling will send big waves across the legal landscape.

If the ruling is adopted broadly or not, we believe it's not only a matter of staying within the law. It goes further than that. We feel that every website owner should respect the privacy of its visitors.

We believe in creating an independent web that is friendly to website visitors. That's why we built [Simple Analytics](https://simpleanalytics.com/simpleanalytics.com), a [privacy-first Google Analytics alternative](https://www.simpleanalytics.com/blog/why-simple-analytics-is-a-great-alternative-to-google-analytics) that is cookieless by design and does not collect any personal data while providing the insights you need. If this resonates with you, feel free to [give us a try](https://simpleanalytics.com/welcome).

> [^footnote]: The Court actually referred to both the GDPR and the older Data Protection Directive in this case, but stated that there is no significant difference between the relevant Articles of the GDPR and the Directive. It’s perfectly safe to treat this case as a GDPR case, as we do in our post.
