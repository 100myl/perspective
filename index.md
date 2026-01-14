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
<<article class="post-preview">
  <h2>
    <a href="{{ site.baseurl }}{{ post.url }}">
      {{ post.title }}
    </a>
  </h2>

  <p class="meta">
    <i class="fa-regular fa-calendar"></i>
    {{ post.date | date: "%B %d, %Y" }}
    · <i class="fa-regular fa-clock"></i> 5 min read
  </p>

  <p class="excerpt">
    {{ post.excerpt | strip_html | truncate: 160 }}
  </p>

  <div class="post-actions">
    <button>
      <i class="fa-regular fa-heart"></i> Like
    </button>
    <button>
      <i class="fa-solid fa-share"></i> Share
    </button>
  </div>
</article>
>
{% endfor %}
