---
layout: single
title: "News"
permalink: /news/
---

{% for post in site.posts %}
### {{ post.date | date: "%B %Y" }} — {{ post.title }}

{{ post.excerpt }}

{% unless forloop.last %}<hr>{% endunless %}
{% endfor %}
