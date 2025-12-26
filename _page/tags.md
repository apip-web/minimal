---
layout: default
title: Tags
permalink: /tags/
---

<h1>Tags</h1>

<ul>
  {% assign tags = site.tags | sort %}
  {% for tag in tags %}
    <li id="{{ tag[0] }}">
      <strong>{{ tag[0] }}</strong>
      <ul>
        {% for post in tag[1] %}
          <li>
            <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
          </li>
        {% endfor %}
      </ul>
    </li>
  {% endfor %}
</ul>
