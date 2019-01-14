---
title: How I made a mistake and what I did about it
author_slug: adriaan
author: Adriaan van Rossum
---

When your building new features you probably want to deploy them as fast as possible because you're too excited to show them to your customers. Or sometimes you're adding a new service to your server and you didn't know what kind of implication it could have. The last happened to me.

Last few weeks back I deployed a new feature called _Custom domain_. This feature allows users of Simple Analytics to bypass ad blockers and tracking blockers. I believe people should be allowed to block tracking so Simple Analytics respects the Do Not Track setting of the browser. Unfortunately Simple Analytics is added to some privacy blocking lists, which I think is not fair because we take privacy very seriously (moved the servers to a very privacy friendly country: Iceland; encrypted our database server; actually delete data from the database when a user deletes something; allow people to download their data). After this feature was deployed a few users started using it.

<img class="limit-height" src="/images/bug.svg" alt="">

Today I found a bug (thankfully by myself) when using the _Custom domain_-feature where the JavaScript was loading, but the API call did ask for a password. I looked up one of my customers' websites ([excuseme.wtf](https://excuseme.wtf/?ref=blog.simpleanalytics.io)) from who I know is using the _Custom domain_-feature. I checked [his stats](https://simpleanalytics.io/excuseme.wtf) and was terrified when I saw no visits for the last week. Immediately I started diggin' in my servers and trying to look for clues.

### Current setup

Simple Analytics uses 4 servers to keep everything running as smooth as possible. We have the Queue server which is the server for collecting the visits from our JavaScripts. This is a different server from the Main server because the Main server is encrypted. If a server is encrypted it should only boot after entering a password (otherwise the encryption is useless). When the unlikely event of a reboot takes place I want to guarantee zero data loss. All data will be sent to the Queue server which will send it to the Main server. If the Main server will not accept the request the Queue server will "queue" (save) the request for when the Main server is back up.

Next, to these servers, I have a Testing server and External server. The Testing server runs acceptance tests to monitor important flows and endpoints. The External server is needed for the _Custom domain_-feature. Due to [separation of concerns](https://en.wikipedia.org/wiki/Separation_of_concerns) I don't want to have customer SSL certificates on the same server as the Main server.

### What went wrong?

I added a new monitoring app to the Queue server, this way I could remotely look if there where any problems in the server. It also gave me insights into CPU and memory use. I added an NGINX configuration file for this app so I could access it from outside. When added a new app I always test the NGINX configuration and reload it when succeeded `sudo nginx -t && sudo nginx -s reload`. NGINX didn't give any error and I could access my new installed monitoring app; I'm happy.

Luckily I have NGINX logs, from where I can get most of the lost request back. These logs contained less information at the time and only showed the time, URL, and user agent.

<img class="limit-height" src="/images/server.svg" alt="">

### What did I do to prevent this from happening?

While this bug didn't affect a lot of customers and didn't have a lot of data loss, I want to do everything I can to prevent this from happening. The bug was created by adding another app to the same server which where no server directive was been defined as the default server. NGINX then tries it's best to select a server as the default server and sends the requests to the app defined in that server.

So first I added the default_server to the listen directive for port 80 and 443 in the main app ([nginx docs](https://nginx.org/en/docs/http/server_names.html#miscellaneous_names)). The main app on that server was the external app that manages the certificates for the _Custom domain_-feature and replies with a script and API endpoint does not use Simple Analytics URLs which makes it hard to block. 

Another thing I did was increasing the log history to 90 days so I can recover visits for future issues. The Queue-server and the Main-server now logs everybody of every failed request. This means every request that returns a TTP code `5xx` or `4xx` will be saved in the logs and can be recovered from it. It will require quite some work to get it done, but it means no data loss.

I added acceptance tests for the _Custom domain_-feature which checks if both the endpoints are still working as expected. If that's is not the case I will get a phone call and a Telegram message.

As the last thing I'm going to tag new features as beta, so customers know it could error and has not been tested to be called stable. Then it's up to the customer to take the risk and use the feature.

I contacted the customers that where affected by this bug and offered them their money back for the month. They didn't found that necessary and said I shouldn't worry about it. I did my best to recover most of their data and with all the above actions I pretty sure this will not happen again.
