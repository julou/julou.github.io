---
layout: default
title: About
permalink: /
---

{% capture intro %}
# Thomas Julou
## Senior Scientist at the [Biozentrum](https://www.biozentrum.unibas.ch/research/groups-platforms/overview/unit/nimwegen/) (Basel)

In my research, I use microbes to address questions related to phenotypic variability, _i.e._ to study the range of phenotypes realised by microbial cells with the same genetic information in the same environment. My interests and [projects](#projects) range from the molecular mechanisms underlying phenotypic variability to its evolutionary implications for microbial populations. Beyond their fundamental interests, understanding these questions is also critical to prevent the emergence of antibiotics “persistence” and to optimise synthesis processes in biotechnological industries.

In practice, I use and develop single-cell methodologies – primarily based on microfluidics, quantitative light microscopy and quantitative flow cytometry. Moreover, I cherish a very tight integration of the experimental and modelling components for every project. I implement and promote [reproducible practices](resources) for experimental research and data analysis, and rely as much as possible on open source tools.

Have overlapping interests? Want to learn about these approaches? Please [contact me](#contact) to discuss current opportunities to work together. In particular, I always welcome applications of talented and enthusiastic students and postdocs.

{%- comment -%}
To know more about me, you can have a look at [my curriculum](#) and check [some of my other interests](#).
{%- endcomment -%}
{% endcapture %}


{% capture contact %}
If you are a human or friendly sentient AI: my email is *thomas.julou*, followed immediately by *@normalesup.org*

Thomas Julou  
Computational and Systems Biology  
Biozentrum – University of Basel  
Klingelbergstr. 50/70  
4056 Basel  
Switzerland

<hr>

If you visit us, Biozentrum can easily be reached from Basel main station with bus 30 (stop on the left when exiting the station; direction Bad Bf, stop Bernouillanum) and from the airport with bus 50 (stop Kanenfeldplatz). Our lab is on the 6th floor of Pharmazentrum (room PZ6020).
{% endcapture %}


<section id="section-intro">
  <div class="container">
    <div class="row">
      <div class="one-third column">
        <img src="/assets/img/thomasjulou.jpg">
        <p class="img-credit">photo by G. Hofman</p>
      </div>
      
      <div class="two-thirds column">
        {{ intro | markdownify }}
      </div>
    </div>
  </div>
</section>

<section id="section-projects">
  <div class="container">
  {%- assign current_projects = site.projects | where:"past",false -%}
  {%- assign past_projects = site.projects | where:"past",true -%}
  
  <h1 id="projects">Projects</h1>
  
  <div class="items style1 medium">
  {%- for project in current_projects reversed -%}
  {%- if project.published -%}
     <div class="project">
      <h2>{{ project.title }}</h2>
        <p><i>with {{ project.collaborators }}.</i></p>
        <p>{{ project.content }}</p>
    </div>
  {%- endif  -%}
  {%- endfor -%}
  </div>
  
  
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

<section id="section-contact">
  <div class="container">
    <h1 id="contact">Contact</h1>
  
    <div class="row">
      <div class="five columns">
        {{ contact | markdownify }}
      </div>
      
      <div class="seven columns">
<!--        <iframe width="100%" height="450" frameborder="0" style="border:0"
  src="https://www.google.com/maps/embed/v1/place?q=Biozentrum&key=AIzaSyBhmRrxYN0evi_9JniNSGhJ7NFYFOAZyOs" allowfullscreen></iframe> -->
        <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d1378405.7892098576!2d6.459358450004041!3d47.56392017918194!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x4791b908135df8df%3A0x850b8df911af1a74!2sBiozentrum+der+Universit%C3%A4t+Basel!5e0!3m2!1sen!2sch!4v1515367261276" width="100%" height="450" frameborder="0" style="border:0" allowfullscreen></iframe>
      </div>
    </div>
  </div>
</section>
