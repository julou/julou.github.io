---
layout: default
title: Past Projects
permalink: /archive/
---

{%- assign past_projects = site.projects | where:"past",true -%}

<section>
  <div class="container">
  <h1>Past projects</h1>
  
  <div class="items style1 medium">
  {%- for project in past_projects reversed -%}
  {%- if project.published -%}
    <div class="project">
      <h2>{{ project.title }}</h2>
        <p><i>with {{ project.collaborators }}.</i></p>
        <p>{{ project.content }}</p>
    </div>
  {%- endif  -%}
  {%- endfor -%}
  </div>
  </div>
</section>

