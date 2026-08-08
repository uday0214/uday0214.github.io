---
layout: page
title: TIL
permalink: /til/
kicker: Learning log
description: Small discoveries worth remembering, captured while studying and building.
wide: true
---

{% assign til_count = 0 %}
<div class="post-feed">
  {% for post in site.posts %}
    {% if post.categories contains "til" %}
      {% assign til_count = til_count | plus: 1 %}
      {% include post-card.html post=post %}
    {% endif %}
  {% endfor %}

  {% if til_count == 0 %}
    <div class="empty-state">
      <p class="eyebrow">Nothing published yet</p>
      <h3>Short learning notes will appear here.</h3>
      <p>Add <code>categories: til</code> to a post’s front matter to include it in this collection.</p>
    </div>
  {% endif %}
</div>
