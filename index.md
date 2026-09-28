---
layout: default
title: About Me
---

<div class="about-layout">
  <aside class="about-sidebar">
    <img class="headshot" src="{{ '/assets/images/headshot.svg' | relative_url }}" alt="Placeholder headshot">

    <div class="contact-icons">
      <a class="icon-badge" href="mailto:{{ site.author.email }}" title="Email" aria-label="Email">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
          <rect x="2" y="4" width="20" height="16" rx="2"/>
          <path d="m22 6-10 7L2 6"/>
        </svg>
      </a>
      <a class="icon-badge" href="https://github.com/{{ site.author.github }}" target="_blank" rel="noopener" title="GitHub" aria-label="GitHub">GH</a>
      <a class="icon-badge" href="https://twitter.com/{{ site.author.twitter }}" target="_blank" rel="noopener" title="Twitter / X" aria-label="Twitter / X">X</a>
      <a class="icon-badge" href="https://linkedin.com/in/{{ site.author.linkedin }}" target="_blank" rel="noopener" title="LinkedIn" aria-label="LinkedIn">in</a>
      <a class="icon-badge" href="{{ '/feed.xml' | relative_url }}" target="_blank" rel="noopener" title="RSS feed" aria-label="RSS feed">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
          <path d="M4 11a9 9 0 0 1 9 9"/>
          <path d="M4 4a16 16 0 0 1 16 16"/>
          <circle cx="5" cy="19" r="1.5" fill="currentColor" stroke="none"/>
        </svg>
      </a>
    </div>
  </aside>

  <div class="about-body" markdown="1">
# About Me

Hi! I'm an astronomy graduate student at The Ohio State University. I'm primarily interested in charting the properties and evolution of stars, including the orbits of close-in binaries, the occurrence relation of stellar flares & spots, and the presence of sympathetic flares. 

My present research is on improving corrections to the saturated stars pipeline of the All-Sky Automated Survey for Supernovae (ASAS-SN) collaboration. I also like to work on the instruments which produce our astronomical data, and am currently characterizing persistence on the iLocater spectrograph. 
  </div>
</div>

<div class="section-heading">
  <h2>Featured projects</h2>
  <a class="section-link" href="{{ '/projects/' | relative_url }}">All projects &rarr;</a>
</div>

<ul class="card-grid">
{% for project in site.projects limit:3 %}
  <li class="card">
    <img class="card-media" src="{{ '/assets/images/preview-icon.svg' | relative_url }}" alt="">
    <div class="card-content">
      <a class="card-title" href="{{ project.url | relative_url }}">{{ project.title }}</a>
      {% if project.summary %}<p class="post-excerpt">{{ project.summary }}</p>{% endif %}
    </div>
  </li>
{% endfor %}
</ul>

<div class="section-heading">
  <h2>Recent posts</h2>
  <a class="section-link" href="{{ '/photography/' | relative_url }}">All posts &rarr;</a>
</div>

<ul class="card-grid">
{% for post in site.posts limit:5 %}
  <li class="card">
    <a class="card-media-link" href="{{ post.url | relative_url }}">
      <img class="card-media" src="{{ post.image | relative_url }}" alt="">
    </a>
    <div class="card-content">
      <span class="post-date">{{ post.date | date: "%b %-d, %Y" }}</span>
      <a class="card-title" href="{{ post.url | relative_url }}">{{ post.title }}</a>
      {% if post.excerpt %}
        <p class="post-excerpt">{{ post.excerpt | strip_html | truncatewords: 24 }}</p>
      {% endif %}
    </div>
  </li>
{% endfor %}
</ul>

