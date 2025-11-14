---
layout: default
title: "Home"
---
# Welcome to My Simple Blog
Here are my posts:
{% for post in site.posts %}
<a href="{{ post.url | relative_url }}">{{ post.title }}</a>
{% endfor %}
