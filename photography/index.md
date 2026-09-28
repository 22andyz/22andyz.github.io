---
layout: default
title: Photography
permalink: /photography/
---

# ✦ Photography

<ul class="card-grid">
{% for post in site.posts %}
  <li class="card">
    <a class="card-media-link" href="{{ post.url | relative_url }}">
      <img class="card-media" src="{{ post.image | relative_url }}" alt="">
    </a>
    <div class="card-content">
      <span class="post-date">{{ post.date | date: "%b %-d, %Y" }}</span>
      <a class="card-title" href="{{ post.url | relative_url }}">{{ post.title }}</a>
      {% if post.excerpt %}
        <p class="post-excerpt">{{ post.excerpt | strip_html | truncatewords: 30 }}</p>
      {% endif %}
    </div>
  </li>
{% endfor %}
</ul>
