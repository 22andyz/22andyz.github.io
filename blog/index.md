---
layout: default
title: Blog
permalink: /blog/
---

<div class="hero-eyebrow">✦ Log</div>

# Blog

<ul class="card-grid">
{% for post in site.posts %}
  <li class="card">
    <span class="post-date">{{ post.date | date: "%b %-d, %Y" }}</span>
    <a class="card-title" href="{{ post.url | relative_url }}">{{ post.title }}</a>
    {% if post.excerpt %}
      <p class="post-excerpt">{{ post.excerpt | strip_html | truncatewords: 30 }}</p>
    {% endif %}
  </li>
{% endfor %}
</ul>
