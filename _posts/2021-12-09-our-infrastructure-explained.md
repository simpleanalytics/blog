---
title: Our infrastructure explained
author_slug: adriaan
author: Adriaan van Rossum
draft: true
# excerpt: ""
# image: https://assets.simpleanalytics.com/blog/ethicalads/social-media.png
---

En wat betreft settings, dit zou goed moeten zijn voor 3 nodes, toch?

```
"refresh_interval": "10s",
"number_of_shards": "1",
"number_of_replicas": "2"
```

Dan kunnen er in theorie 2 uitvallen zonder data verlies.

### Shards

When you're using Elasticsearch you don't need to know about shards that much. Until you do. We started using Elasticsearch with a single node setup. It worked great for our use-case. We came from PostgreSQL which worked fine, but at some point the caching tables got out of hand.

Shards are basically like tables you have in an Excel sheet. If you have many small tables, you create overhead
