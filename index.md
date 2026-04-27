---
layout: default
title: Blogs about Homelabs, data, and tech
---

A little blog to help document my work

## Recent Posts
<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      <span>{{ post.date | date_to_string }}</span>
    </li>
  {% endfor %}
</ul>