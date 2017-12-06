---
layout: page
title: Projects
# navigation_weight: -7
---

# Current projects

{% for project in site.projects reversed %}
{% if project.published %}
{% unless project.archive %}
  <h2>{{ project.title }}</h2>
  <p><i>with {{ project.collaborators }}.</i></p>
  <p>{{ project.content }}</p>
<!--  <p><a href="{{ project.url }}">{{ project.title }}</a></p> -->
{% endunless %}
{% endif  %}
{% endfor %}


# Archive

{% for project in site.projects reversed %}
{% if project.published %}
{% if project.archive %}
  <h2>{{ project.title }}</h2>
  <p><i>with {{ project.collaborators }}.</i></p>
  <p>{{ project.content }}</p>
<!--  <p><a href="{{ project.url }}">{{ project.title }}</a></p> -->
{% endif  %}
{% endif  %}
{% endfor %}
