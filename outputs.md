---
layout: default
title: Outputs
permalink: /outputs/
lightgallery: true
---

{% capture _gallery %}
## Gallery

*Let's start with the fun bit: here are videos and pictures showcasing various aspects of my [research projects](/#projects)*.
{% include gallery.html %}

{%- comment -%}
- ceftriaxone
- temp gradient
{%- endcomment -%}
{% endcapture %}


{% capture _publications %}
## Publications

_This list might be neither exhaustive nor up-to-date: you can also find me on [google scholar](https://scholar.google.com/citations?user=prpTE68AAAAJ)._

{% include bibArticles.html %}
{% endcapture %}


{% capture _communications %}
## Talks & Posters

{% include bibPresentations.html %}
{% endcapture %}


{% capture _tools %}
## Tools

- [MoMA](https://github.com/fjug/MoMA/wiki) a.k.a. the **Mo**ther **M**achine **A**nalyzer, written by [Florian Jug](https://www.mpi-cbg.de/research-groups/current-groups/florian-jug/group-leader/) in collaboration with our lab: a state-of-the-art image analysis software to track bacteria growing in microfluidics channels. 
- [DIMM](https://metafluidics.org/devices/dual-input-mother-machine/) a.k.a the **D**ual **I**nput **M**other **M**achine: a microfluidics design for long-term growth and monitoring in precisely controlled environmental conditions.
{% endcapture %}
- a [collection of scripts and configuration files](https://github.com/vanNimwegenLab/MiM_NikonTi) for quantitative light microscopy using [Micro-Manager](https://micro-manager.org).
- a [minimalist R package](https://github.com/julou/ggCustomTJ) to tweak ggplot2 to my taste.
- a [lightweight, responsive website template](https://github.com/julou/julou.github.io) based on the Skeleton boilerplate (no javascript — except for media lightbox, no jQuery dependency, no Bootstrap dependency: loading a page transfers less than 200kb!). You're currently looking at it ;)

{% capture _data %}
## Data

- [Images and raw data](https://doi.org/10.5281/zenodo.824793) for [Kaiser M, Jug F, Julou T, <i>et al.</i>, <i>Nat Commun</i>. <b>9</b>, 212 (2018)](https://doi.org/10.1038/s41467-017-02505-0).
{% endcapture %}


<section id="section-gallery">
  <div class="container">
    <h1>Outputs</h1>
    
    {{ _gallery | markdownify }}
  </div>
</section>

<section id="section-publns">
  <div class="container">
    <div class="row">
      <div class="one-half column not-narrow">
        {{ _publications | markdownify }}
      </div>
      <div class="one-half column not-narrow">
        {{ _communications | markdownify }}
      </div>
    </div>
  </div>
</section>

<section id="section-shared">
  <div class="container">
    <div class="row">
      <div class="one-half column">
        {{ _tools | markdownify }}
      </div>
      <div class="one-half column">
        {{ _data | markdownify }}
      </div>
    </div>
  </div>
</section>
