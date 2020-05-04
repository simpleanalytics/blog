---
title: Why I share my failure at the risk of losing customers
author_slug: adriaan
author: Adriaan van Rossum
---

As the owner of Simple Analytics, I think it’s super important to build user trust. It’s nearly impossible not to make any mistakes, so if a company never shares their mistakes, they are probably not telling you the truth. Hence, here are mine.

Whenever you're building new feature, you probably want to deploy them as fast as possible because you're too excited to show them to your customers. Or sometimes you're adding a new service to your server and you didn't know what kind of implication it could have. The latter happened to me.

In the past couple of weeks I deployed a new feature called _Custom domain_. This feature allowed users of Simple Analytics to bypass ad-blockers and tracking blockers. I believe people should be allowed to block tracking, so Simple Analytics respects the "Do Not Track" setting of the browser. Unfortunately, Simple Analytics has been added to some privacy block lists - which I think is not fair since we take privacy very seriously (moved the servers to a very privacy friendly country: Iceland; encrypted our database server; It removes data from the database when a user deletes something; allowing people to download their data). So the new feature was very welcomed. Once it was deployed, a few users started using it.

<img loading="lazy" class="limit-height" src="/images/bug.svg" alt="">

Today I found a bug (thankfully by myself) when using the _Custom domain_-feature where the JavaScript was loading, but the API-call asked for a password. I looked up one of my customers' websites ([excuseme.wtf](https://excuseme.wtf/?ref={{ site.hostname }})) who I know was using the _Custom domain_-feature. I checked [his stats](https://simpleanalytics.com/excuseme.wtf) and was horrified to find out there weren't any visits for the last week. Immediately I started digging into my servers, looking for clues.

### Current setup

Simple Analytics uses 4 servers to keep everything running as smooth as possible. We have the Queue-server, which is the server for collecting the visits from our JavaScripts. This is a different server from the Main-server because the Main-server is encrypted. If a server is encrypted it should only boot after entering a password (otherwise the encryption is useless). During an unlikely event, a reboot is required, I want to guarantee zero data loss. All data will be sent to the Queue-server that will send it to the Main-server. If the Main-server will not accept the request the Queue-server will "queue" (save) the request when the Main-server is backing up.

Next, to these servers, I have a Testing-server and External-server. The Testing-server runs acceptance tests to monitor important flows and endpoints. The External-server is needed for the _Custom domain_-feature. Due to [separation of concerns](https://en.wikipedia.org/wiki/Separation_of_concerns) I don't want to have customer SSL certificates on the same server as the Main-server for security reasons.

### What went wrong?

I decided to install a new monitoring app to the Queue-server, this way I could check remotely if there where any problems in the server. It also gave me insights into CPU and memory use. I added an NGINX configuration file for this app so I could access it from outside. When adding a new app I always test the NGINX configuration and reload it when succeeded `sudo nginx -t && sudo nginx -s reload`. NGINX didn't give any error therefore, I could access my newly installed monitoring app; I'm happy.

Luckily, I have a directory/records of NGINX logs, from where I can retrieve most of the lost request back. These logs contained less information at the time and only recorded the time, URL, and user agent.

<img loading="lazy" class="limit-height" src="/images/server.svg" alt="">

### What did I do to prevent this from happening again?

While this bug didn't affect a lot of customers and didn't have a significant amount of data loss, I want to do everything I can to prevent this from happening in the future. The bug was created by adding another app to the same server which didn't have any server directive being defined as the default server. NGINX then tries it's best to select a server as the default server and sends the requests to the app defined in that server.

Firstly, I added the default server to the listen directive for port 80 and 443 in the main app ([nginx docs](https://nginx.org/en/docs/http/server_names.html#miscellaneous_names)). The main app on that server was the external app that manages the certificates for the _Custom domain_-feature and replies with a script and API endpoint does not use Simple Analytics URLs which makes it hard to block.

Secondly, I increased the log history to 90 days so I can recover visits for future issues. The Queue-server and the Main-server now logs every failed request by anyone. This means every request that returns a HTTP code `5xx` or `4xx` will be saved in the logs and can be recovered from it. It will require quite some work to get it done if needed, but it means no data loss.

I added acceptance tests for the _Custom domain_-feature that checks if both the endpoints are still working as expected. If they don't comply, I would get a phone call and a Telegram message.

Lastly, I'm going to tag new features as "Beta version", so customers are aware or expected it to have errors as it would not have been completed for final relsease. Hence, it's up to the customers to take the chance and use the feature at their own risk.

I have contacted the customers that where affected by this bug and offered them their money back for the month. They didn't find that necessary and said I shouldn't worry about it. I did my best to recover most of their data and with all the above actions I'm pretty sure this will not happen again.

Let’s change the transparency around mistakes and I believe people will take your business more seriously. You show what you did about it and how capable you are. Some people would argue if it's smart, but I see this as an opportunity to show transparency.
