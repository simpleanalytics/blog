---
title: How I made a big mistake and what I did about it
---

When your building new features you probably want to deploy them as fast as possible because you're excited to show them to your customers. Or sometimes you're adding a new service to your server and didn't know what kind of implication it could have.

Last week I deployed a new feature called _"Custom domain"_. This features allows users of Simple Analytics to bypass ad-blockers and tracking-blockers. I believe people should be allowed to block tracking so Simple Analytics respects the Do Not Track setting of the browser. Simple Analytics is put on privacy blocking hostname lists, which I think is not fair, because we take privacy very seriously (moved the servers to a very privacy friendly country: Iceland; excrypted our database server; actually delete data from database when user deletes something; allow people to download their data). After this feature was deployed a few users started using it. 

<img class="limit-height" src="/images/server.svg" alt="">

Today I found a bug (thankfully by myself) where the JavaScript was still loaded, but the API call did fail. I looked up one of my customers' website ([excuseme.wtf](https://excuseme.wtf/?ref=blog.simpleanalytics.io)) from who I know is using the _"Custom domain"_ feature. I checked [his stats](https://simpleanalytics.io/excuseme.wtf) and was terrified when I saw no visits for the last week. Immediately I started diggin' in my servers and trying to look for clues.

I added a new monitoring app to the queue server. I also added a NGINX configuration file for this app so I could access it from outside. When added a new app I always test the NGINX configuration and reloading it when succeeded `sudo nginx -t && sudo nginx -s reload`. NGINX didn't give any error and I could access my new installed monitoring app.

What did I do to prevent this from happening?

- Set default_server to listen directive for port 80 and 443 in main app ([nginx docs](https://nginx.org/en/docs/http/server_names.html#miscellaneous_names))
- Increased the syslog history to 90 days so I can recover visits from future issues
- Added a test script for a _"Custom domain"_ which checks every 60 seconds if the API and script are accessable and warns me via a phone call and Telegram notification when it fails

### What did I learn from this?

- I didn't tag the _"Custom domain"_ feature as beta (which I definitely will in the future).
