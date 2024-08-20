---
layout: default
title: Blog
permalink: /blog/
---

<style>
  .blog-list {
    list-style-type: none;
    padding: 0;
  }
  .blog-post {
    background-color: #f8f9fa;
    border-radius: 8px;
    padding: 20px;
    margin-bottom: 20px;
    box-shadow: 0 2px 5px rgba(0,0,0,0.1);
    transition: transform 0.3s ease;
  }
  .blog-post:hover {
    transform: translateY(-5px);
  }
  .blog-title {
    color: #007bff;
    text-decoration: none;
    font-size: 24px;
    margin-bottom: 10px;
    display: block;
  }
  .blog-date {
    color: #6c757d;
    font-size: 14px;
    margin-bottom: 10px;
  }
  .blog-description {
    color: #333;
    line-height: 1.6;
  }
</style>

# Blog Posts

<ul class="blog-list">
{% for post in site.posts %}
  <li class="blog-post">
    <a href="{{ post.url | relative_url }}" class="blog-title">{{ post.title }}</a>
    <p class="blog-date">{{ post.date | date: "%B %d, %Y" }}</p>
    <p class="blog-description">{{ post.description | default: post.content | strip_html | truncatewords: 50 }}</p>
  </li>
{% endfor %}
</ul>

