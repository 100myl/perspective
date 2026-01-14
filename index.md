---
layout: default
title: Home
---

{% for post in site.posts %}
<article class="post-preview">
  <h2>
    <a href="{{ site.perspective }}{{ post.url }}">
      {{ post.title }}
    </a>
  </h2>

  <p class="meta">
    {{ post.date | date: "%B %d, %Y" }} · 5 min read
  </p>

  <p class="excerpt">
    {{ post.excerpt | strip_html | truncate: 160 }}
  </p>
</article>
{% endfor %}
