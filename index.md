---
layout: default
title: "Home"
---

# Welcome to My Blog

Here are my posts:

{% for post in site.posts %}
<a href="{{ post.url }}">{{ post.title }}</a>
{% endfor %}
