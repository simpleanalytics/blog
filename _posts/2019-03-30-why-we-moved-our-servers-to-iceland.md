---
title: Why we moved our servers to Iceland
author_slug: adriaan
author: Adriaan van Rossum
---

<blockquote role="alert" markdown="1">
  This blog post is outdated. In the meantime we moved our servers from Iceland to The Netherlands. [Here is why](https://docs.simpleanalytics.com/locations).
</blockquote>

As the founder of Simple Analytics, I have always been mindful for the need of trust and transparency for our customers. We would like to be held accountable for our customers needs, so they can sleep in peace. The choices we make has to be optimal, in terms of privacy, for the visitors and our customers. One of the crucial choices to consider was, choosing the location of our servers.

<img loading="lazy" class="limit-height" src="/images/flag-map-of-iceland.svg" alt="">

In the last few months, we moved our servers gradually to Iceland. In this blog post, I'd like to explain how we've achieved that, and most importantly, why. It wasn't an easy process and I would like to share our learnings. There are some technical parts in this article which I've tried to write in an understandable way, but forgive me if it's too technical.

## Why moving our servers?

It all started with our website being added to [EasyList](https://easylist.to/). It's a list with domain names which are used by popular ad-blockers. I asked why Simple Analytics was added, because we don't track visitors of our customers' websites. We even [respect](https://github.com/simpleanalytics/cdn.simpleanalytics.io/blob/fae87364ae6dc2e26827fb9438745a8ac0c8024d/hello.js#L41-L42) the "Do Not Track" settings in the browser.

So I [replied the following](https://github.com/easylist/easylist/pull/1855#issuecomment-440241758) to the [Pull Request on GitHub](https://github.com/easylist/easylist/pull/1855):

> [...] So if we keep blocking the companies that do good, and respect the privacy of the users, what kind of sign is it to just block those companies? I think it's wrong and we shouldn't put every company on the list just because they are sending a request. [...]

I got [a reply](https://github.com/easylist/easylist/pull/1855#issuecomment-440251257) to my comment from [@cassowary714](https://github.com/cassowary714):

> Everyone says what you are saying, but I don't want to see my requests sent to a US company (in your case, Digital Ocean [...]

I didn't like this reply at first, but after sharing it with my community people pointed it out to me that he indeed was correct about the fact the US government is able to access the data of our users. At that time, our servers were indeed running on Digital Ocean and they could pull out our drive and read our data.

<img loading="lazy" class="limit-height" src="/images/safe.svg" alt="">

The solution is somewhat technical so bear with me. You can make a stolen drive (or detached for whatever reason) unusable for others. This can be solved by encrypting the data on the drive which makes it very difficult to read the data for people without the encryption key _(Note: only Simple Analytics has this key)._ It would still be possible to get little parts of the data by physically reading out the memory of the server. Memory is easy explained as a type of a drive, which is small but super fast which allows the processor of the server to run efficiently. A server does not function without memory so we kind of need to trust the hosting provider.

This challenged me to think where to move our servers.

## Our next location

I started with some basic searches and found a Wikipedia page on [Internet censorship and surveillance by country](https://en.wikipedia.org/wiki/Internet_censorship_and_surveillance_by_country#Reporters_Without_Borders). It contains a list of "Enemies of the Internet" by the Reporters without Borders, a Paris-based international non-governmental organization that advocates freedom of the press, which classifies a country as an enemy of the internet when "all of these countries mark themselves out not just for their capacity to censor news and information online but also for their almost systematic repression of Internet users."

Apart from this list, there is an alliance called [Five Eyes](https://en.wikipedia.org/wiki/Five_Eyes) a.k.a. FVEY. It's an alliance of Australia, Canada, New Zealand, the United Kingdom, and the United States. In recent years, documents have shown that they are intentionally spying on one another's citizens and sharing the collected information with each other in order to circumvent restrictive domestic regulations on spying ([sources](https://en.wikipedia.org/wiki/List_of_people_under_Five_Eyes_surveillance#cite_ref-8)). The former NSA contractor Edward Snowden, described the FVEY as a "supra-national intelligence organization that doesn't answer to the laws of its own countries." There are other countries working together with the FVEY in other international cooperatives including Denmark, France, the Netherlands, Norway, Belgium, Germany, Italy, Spain, and Sweden (so-called 14 Eyes). I couldn't find evidence of the 14 Eyes alliance abusing their combined intelligence.

<img loading="lazy" class="limit-height" src="/images/server-down.svg" alt="">

At this point, we were pretty sure not to use any of the listed countries from the "Enemies of the Internet" list and just to be sure to skip the countries on the 14 Eyes alliance list. For Simple Analytics, this gave enough reason to avoid those countries for storing the data of our customers.

The Wikipedia page mentioned earlier reads the following for Iceland:

> Censorship is prohibited by the Icelandic Constitution and there is a strong tradition of protecting freedom of expression that extends to the use of the Internet. [...]

## Iceland

While researching the best country, privacy-wise, Iceland kept popping up. So I did some thorough research on Iceland. Please keep in mind that I don't speak Icelandic which may have resulted in missing important information. [Let us know](https://simpleanalytics.com/feedback) if you have any feedback.

According to the [Freedom on the Net 2018 report](https://freedomhouse.org/report/countries-net-freedom-2018) (from the Freedom House), Iceland together with Estonia scored a 6/100 (lower is better) on the Internet Freedom Score. This makes them one of the best privacy-friendly countries. Be aware that not every country has been rated.

Iceland is not a member of the European Union, although the country is part of the European Economic Area and has agreed to follow legislation regarding consumer protection and business law similar to other member states. This includes the Electronic Communications Act 81/2003 which implemented data retention requirements.

The law applies to telecommunication providers and mandates the retention of records for six months. It also states that companies may only deliver information on telecommunications in criminal cases or on matters of public safety and that such information may not be given to anyone other than the police or the public prosecution.

Although, Iceland is somewhat following the laws of the European Economic Area, it has its own approach to privacy. For example, the [Icelandic Data Protection Act](https://www.personuvernd.is/information-in-english/greinar/nr/438) encourages anonymity of user data. ISPs and content hosts are not held legally liable for the content that they host or transmit. According to Icelandic law, its not the domain name provider, but the registrant of an .is domain name that is responsible for ensuring the use of the domain is within the limits of the law ([ISNIC](https://www.isnic.is/en/domain/rules)). The government does not place any restrictions on anonymous communication and no registration is required when purchasing a SIM card.

<img loading="lazy" class="limit-height" src="/images/world-line-sf-ams.png" alt="">

Another advantage from moving to Iceland is the climate and location of the country. Servers produce a lot of heat and Reykjavík (Iceland's capital, where most data centers are located) is on average 40.41°F (4.67°C), meaning it's a great location to cool down the servers. For each watt used to run servers, storage and network equipment, proportionally very little is used for cooling, lighting and other overhead. On top of that, Iceland is the world's largest green energy producer per capita and largest electricity producer per capita, with approximately 55,000 kWh per person per year. In comparison, the EU average is less than 6,000 kWh. Most hosting providers in Iceland get 100% of their electricity from renewable energy sources.

If you draw a straight line from San Francisco to Amsterdam you will cross Iceland. Simple Analytics has most customers from the US and Europe, so it makes sense to pick this geographical location. The privacy-friendly laws and the environmental friendly approach of Iceland made it even more easy for us to choose them as the new location for our servers.

## Moving our servers

First, we needed to find a hosting provider in Iceland. There are quite a few, and it's really hard to know if you have the best. We didn't have the resources to try them all, so instead, we set up some automatic scripts ([Ansible](<https://en.wikipedia.org/wiki/Ansible_(software)>)) while setting up the server so we could easily move to another provider if we needed to. We choose [1984](https://1984hosting.com/), a company with the slogan "Safeguarding privacy and civil rights since 2006". We liked that slogan and asked them a few questions about how they would handle our data. They reassured us, and we proceeded installing our main server and they only use electricity from renewable energy sources.

<img loading="lazy" class="limit-height" src="/images/server-status.svg" alt="">

However, we hit a few roadblocks during this process. This section of the article is quite technical. Feel free to skip to the next. When you have an encrypted server you'll need to unlock it with a private key. This key can't be stored on the server as it defeats the purpose of encrypting. So if the key isn't on the server you need to enter it remotely. That's right, we need to enter the key when the server boots. Wait, but what happens with a power failure? Are all requests with page views to your server failing after a reboot?

That's why we added an extra server in front of the main server. This server is kind of stupid. It just receives the requests with page views and sends it directly to our main server. When the main server is failing it will store the requests in its own database and re-attemps those requests to the main server until it succeeds. So after a power failure, there is no data loss anymore.

Back to booting up the server. When the encrypted main server boots we need to enter a password. But we don't want to travel to Iceland or ask somebody there to enter it, for obvious reasons. To access a server remotely you usually use SSH. SSH - is a secure communication protocol, that most people use to communicate with their servers. SSH is a program which is accessible when a server or computer is running. But we needed it to connect before the server was completely started.

Then we found [Dropbear](https://matt.ucc.asn.au/dropbear/dropbear.html), a very small SSH program, that you can run via the [initial ramdisk](https://en.wikipedia.org/wiki/Initial_ramdisk) (initramfs). This means we are able to allow external connections via SSH. We don't have to fly to Iceland to boot our server, yeah!

After moving our data from our old server to our new server in Iceland we were finally done. It took us a couple of weeks from start to end, but we are glad we did it.

## Only storing the data you need

At Simple Analytics we live by the saying: "Only store data you need." We only [collect](http://simpleanalytics.com/what-we-collect) the minimal.

It's common practice to [soft delete](http://abstraction.blog/2015/06/28/soft-vs-hard-delete) data in applications. This means that the data is not really deleted but it's made inaccessible by the end user. We don't do this - if you delete your data, it's gone from our database. We use hard delete. _Note: it will be in our encrypted backups for a maximum of 90 days. In case of a bug we can retrieve this data._

> We don't have delete_at fields ;-)

For customers, it's important to know what data is kept and what is deleted. When somebody deletes their data we show them [a page with exactly that](https://simpleanalytics.com/deleted). We delete the user and their analytics from our database. We also delete the credit card and email from Stripe (our payment provider). We keep the payment history, which is needed for taxes and keep our log files and database backups for 90 days.

<img loading="lazy" class="limit-height" src="/images/personal-data.svg" alt="">

Question: If you only store little sensitive data, what's the need for all this protection and extra security?

Well, we want to be the best privacy focused analytics company in the world. We will do everything within our power to deliver the best analytics tools without invading the privacy of your visitors. By even protecting our massive amounts of unidentifiable information about visitors we want to show we take privacy super seriously.

## What is next?

> Read the discussion <a href="https://news.ycombinator.com/item?id=19526521">on Hacker News</a>

While we improved the privacy of our platform we noticed a slight increase in loading time for our embed scripts. This makes perfect sense, because they were hosted via the CDN of CloudFlare. A CDN is a set of servers around the world to decrease loading times for everybody. We are thinking of setting up a very simple CDN with encrypted servers, which only serve our JavaScript and store the page views temporarily before sending it to our main server in Iceland.

Are you willing to move your business analytics to a privacy-friendly company? [Learn what we can do for you](https://simpleanalytics.com/?ref={{ site.hostname }}).
