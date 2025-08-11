---
layout: default
title: Archives
permalink: /archive/
---

# Archives

## Tous les articles

<ul class="post-list">
  {% for post in site.posts %}
    <li>
      <h3>
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      </h3>
      <p class="post-meta">
        <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%d %B %Y" }}</time>
        {% if post.categories %} • 
          {% for category in post.categories %}
            <span class="category">{{ category }}</span>
          {% endfor %}
        {% endif %}
      </p>
    </li>
  {% endfor %}
</ul>