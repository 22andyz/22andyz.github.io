---
layout: default
title: Projects
permalink: /projects/
---

# ✦ Research Projects

<ul class="card-grid">
{% for project in site.projects %}
  <li class="card">
    <img class="card-media" src="{{ '/assets/images/preview-icon.svg' | relative_url }}" alt="">
    <div class="card-content">
      <a class="card-title" href="{{ project.url | relative_url }}">{{ project.title }}</a>
      {% if project.summary %}<p class="post-excerpt">{{ project.summary }}</p>{% endif %}
    </div>
  </li>
{% endfor %}
</ul>
