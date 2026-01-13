---
layout: default
title: Blog
---

<h1>Blog Posts</h1>

<div class="blog-grid">
  {% for post in site.posts %}
    <a href="{{ post.url | relative_url }}" class="blog-card">
      <h2>{{ post.title }}</h2>
      <p class="date">{{ post.date | date: "%b %d, %Y" }}</p>
      <p class="excerpt">{{ post.excerpt }}</p>
      <span class="read-more">Read More →</span>
    </a>
  {% endfor %}
</div>
