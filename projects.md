---
layout: page
title: Projects
permalink: /projects/
---


{%- assign current_projects = site.projects | where:"past",false -%}
{%- assign past_projects = site.projects | where:"past",true -%}

{%- for project in current_projects reversed -%}
{%- if project.published -%}
   <section class="project">
    <h2>{{ project.title }}</h2>
      <p><i>with {{ project.collaborators }}.</i></p>
      <p>{{ project.content }}</p>
  </section>

  <hr>

{%- endif  -%}
{%- endfor -%}


<h1>Past projects</h1>

{%- for project in past_projects reversed -%}
{%- if project.published -%}
   <section class="project">
    <h2>{{ project.title }}</h2>
      <p><i>with {{ project.collaborators }}.</i></p>
      <p>{{ project.content }}</p>
  </section>

{%- unless forloop.last -%}
  <hr>
{%- endunless -%}

{%- endif  -%}
{%- endfor -%}
