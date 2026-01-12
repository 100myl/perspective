---
layout: default
title: Home
---

# Latest Posts

{% for post in site.posts %}
<div class="post-card">
  <h2>
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
  </h2>
  <p>{{ post.excerpt | strip_html | truncate: 150 }}</p>
</div>
{% endfor %}
