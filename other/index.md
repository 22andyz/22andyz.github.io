---
layout: default
title: Other
permalink: /other/
---

# ✦ Other

<ul class="card-grid">
{% assign other_sorted = site.other | sort: 'date' | reverse %}
{% for item in other_sorted %}
  <li class="card">
    <img class="card-media" src="{{ '/assets/images/preview-icon.svg' | relative_url }}" alt="">
    <div class="card-content">
      {% if item.date %}<span class="post-date">{{ item.date | date: "%b %-d, %Y" }}</span>{% endif %}
      <a class="card-title" href="{{ item.url | relative_url }}">{{ item.title }}</a>
      {% if item.excerpt %}
        <p class="post-excerpt">{{ item.excerpt | strip_html | truncatewords: 30 }}</p>
      {% endif %}
    </div>
  </li>
{% endfor %}
</ul>
