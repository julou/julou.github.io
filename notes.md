---
layout: page
title: Notes
published: false
# permalink: /notes/
# navigation_weight: 5
---

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>
