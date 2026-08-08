---
layout: page
title: Blog
permalink: /blog/
kicker: Writing
description: Long-form articles, technical notes, and deeper writeups from what I learn and build.
wide: true
---

<div class="post-feed">
  {% if site.posts.size > 0 %}
    {% for post in site.posts %}
      {% include post-card.html post=post %}
    {% endfor %}
  {% else %}
    <div class="empty-state">
      <p class="eyebrow">The notebook is open</p>
      <h3>The first article is on its way.</h3>
    </div>
  {% endif %}
</div>
