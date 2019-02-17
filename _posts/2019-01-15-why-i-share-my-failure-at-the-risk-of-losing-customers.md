---
title: Why I share my failure at the risk of losing customers
author_slug: adriaan
author: Adriaan van Rossum
---

As the owner of Simple Analytics, I think it’s super important to build user trust. It’s nearly impossible not to make any mistakes, so if a company never shares their mistake, they are probably not telling you the truth. Hence, here is mine.

Whenever you're building new features, you'd probably want to deploy them as fast as possible, because you're too excited to show them to your customers. Or sometimes you're adding a new service to your server, and you didn't know what kind of implication it could have. The latter happened to me.

In the past couple of weeks I deployed a new feature called _Custom domain_. This feature allows users of Simple Analytics to bypass ad blockers and tracking blockers. I believe people should be allowed to block tracking, so Simple Analytics respects the "Do Not Track" setting of the browser. Unfortunately, Simple Analytics is added to some privacy blocklists - which I think is not fair since we take privacy very seriously (moved the servers to a very privacy friendly country: Iceland; encrypted our database server; removes data from the database when a user deletes something; allows people to download their data). So the new feature was very welcomed. Once it was deployed, a few users started using it.

<img class="limit-height" src="/images/bug.svg" alt="">

Today, I found a bug (thankfully by myself) when using the _Custom domain_-feature where the JavaScript was loading, but the API-call asked for a password. I looked up one of my customers' websites ([excuseme.wtf](https://excuseme.wtf/?ref=blog.simpleanalytics.io)) who I know was using the _Custom domain_-feature. I checked [his stats](https://simpleanalytics.io/excuseme.wtf) and was horrified when I saw there were no visits since last week. I Immediately started digging into my servers, looking for clues. (*what was the conclusion? did you fix it?*)

### Current setup

Simple Analytics, uses 4 servers to keep everything running as smooth as possible. We have the Queue-server, that is the server for collecting the visits from our JavaScripts. Which is a different server from the Main-server because the Main-server is encrypted. If a server is encrypted, it would only boot after entering a password (otherwise the encryption is useless). During an unlikely event a reboot is required, I want to guarantee my users zero data loss. All data will be sent to the Queue server which will send it to the Main server. If the Main server will not accept the request, the Queue server will "queue" (save) the request when the Main server is backed up.

Next, to these servers, I have a Testing-server and External-server. The Testing-server runs acceptance tests to monitor important flows and endpoints. The External-server is needed for the _Custom domain_-feature. Due to [separation of concerns](https://en.wikipedia.org/wiki/Separation_of_concerns) I don't want to have customer SSL certificates on the same server as the Main server for security purposes.

### What went wrong?

I decided to add a new monitoring app to the Queue server, this way I could check remotely if there where any problems in the server. It also gave me insights into CPU and memory use. I added an NGINX configuration file for this app so I could access it from outside. When adding a new app, I always test the NGINX configuration and reload it when succeeded `sudo nginx -t && sudo nginx -s reload`. The NGINX didn't give any error and I could access my newly installed monitoring app; I'm happy.

Luckily, I keep a directory/record* of NGINX logs, where I can retrive most of the lost requests back. Althought, these logs contained less information at the beginning and only recorded the time, URL, and user agent.

<img class="limit-height" src="/images/server.svg" alt="">

### What did I do to prevent this from happening again?

While the bug didn't affect a lot of customers and we didn't have a lot of data loss, I wanted to do everything I could to prevent this from happening in the future. The bug was created by adding another app to the same server, which didnt have any server-directive to be defined as the default server. NGINX then tries it's best to select a server as the default server and sends the requests to the app defined in that server. (this paragraph i dont get what you mean i tried to make edits but pls check if thats what you really mean)

Firstly, I added the default_server to the listen directive for port 80 and 443 in the main app ([nginx docs](https://nginx.org/en/docs/http/server_names.html#miscellaneous_names)). The main app on that server was the external app that manages the certificates for the _Custom domain_-feature and replies with a script and API endpoint does not use Simple Analytics URLs which makes it hard to block. 

Secondly, I increased the log history to 90 days so that I can recover visits for future issues. The Queue-server and the Main-server now logs every failed request by anyone. This means every request that returns a TTP code `5xx` or `4xx` will be saved in the logs and can be recovered from it. It will require quite some work to get it done if needed, but it means no data loss.

I added acceptance tests for the _Custom domain_-feature which checks if both the endpoints are still working as expected. If this is not the case, I will get a phone call and a Telegram message as a precautionary/safety* measure.

Lastly, I'm have decided to tag new features as "Beta version", so customers are aware it might have an error and not been tested to be final version. Therefore, it's up to the consumer to take the risk and use the feature.

I have contacted the customers that where affected by this bug and offered them their money back for the month. They didn't find that necessary and said I shouldn't worry about it. I did my best to recover most of their data and with all the above actions I'm pretty sure this will not happen again.

Let’s change the transparency around our mistakes and people will take your business more seriously. You show them what you did about it and how capable you are. Some people would argue whether this is a smart move or not, but I see this as an opportunity to show transparency.
