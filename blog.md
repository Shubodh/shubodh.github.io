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
  .blog-post.featured {
    border-left: 4px solid #007bff;
    background-color: #f0f8ff;
  }
  .blog-post.featured .blog-title {
    font-size: 26px;
  }
  .featured-tag {
    display: inline-block;
    background-color: #007bff;
    color: white;
    font-size: 12px;
    padding: 3px 8px;
    border-radius: 12px;
    margin-bottom: 10px;
  }


</style>

# Blog Posts

<ul class="blog-list">
{% for post in site.posts %}
  <li class="blog-post {% if post.title == "Mobile Robotics: Navigating from Theory to Application" %}featured{% endif %}">
    {% if post.title == "Mobile Robotics: Navigating from Theory to Application" %}
      <span class="featured-tag">Featured</span>
    {% endif %}
    <a href="{{ post.url | relative_url }}" class="blog-title">{{ post.title }}</a>
    <p class="blog-date">{{ post.date | date: "%B %d, %Y" }}</p>
    <p class="blog-description">{{ post.description | default: post.content | strip_html | truncatewords: 50 }}</p>
  </li>
{% endfor %}
</ul>