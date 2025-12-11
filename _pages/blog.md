---
layout: page
permalink: /blog/
title: blog
nav: true
nav_order: 1
---

<ul class="post-list">
  {% for post in site.posts %}
    <li>
      <span class="post-meta">{{ post.date | date: "%B %d, %Y" }}</span>
      <h3>
        <a class="post-link" href="{{ post.url | relative_url }}">{{ post.title }}</a>
      </h3>
      {% if post.description %}
        <p>{{ post.description }}</p>
      {% endif %}
    </li>
  {% endfor %}
</ul>
