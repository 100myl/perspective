---
layout: default
title: Home
---

<section class="hero">
  <h1>Hi, I’m Pal 👋</h1>
  <p>A personal blog built out of curiosity & learning.</p>
</section>

<h2 class="section-title">Latest Posts</h2>

{% for post in site.posts %}
<div class="post-card">
  <h2>
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
  </h2>
  <p>{{ post.excerpt | strip_html | truncate: 150 }}</p>
</div>
{% endfor %}
