---
layout: default
title: Home
---

# Welcome to Software Cheatsheet

## Blog Posts

{% for post in site.posts %}
  <div>
    <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
    <p><em>{{ post.date | date: "%B %d, %Y" }}</em></p>
    {% if post.excerpt %}
      <p>{{ post.excerpt }}</p>
    {% endif %}
  </div>
{% endfor %}
