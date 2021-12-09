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
