---
layout: page
title: Projects
permalink: /projects/
---


{% for project in site.projects reversed %}
{% if project.published %}
  <section class="project">
    <h2>{{ project.title }}</h2>
      <p><i>with {{ project.collaborators }}.</i></p>
      <p>{{ project.content }}</p>
<!--  <p><a href="{{ project.url }}">{{ project.title }}</a></p> -->
  </section>

{% unless forloop.last %}
  <hr>
{% endunless %}

{% endif  %}
{% endfor %}

