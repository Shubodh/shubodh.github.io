---
layout: default
title: Blog
permalink: /blog/
---

# Blog Posts

{% for post in site.posts %}
	<h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
	<p>{{ post.date | date: "%B %d, %Y" }}</p>
	{{ post.excerpt }}
{% endfor %}