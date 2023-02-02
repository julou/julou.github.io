---
layout: default
title: About
permalink: /
redirect_from:
  - /projects/
  - /contact/
---

{% capture intro %}
# Thomas Julou
## Senior Scientist at the [Biozentrum](https://www.biozentrum.unibas.ch/research/groups-platforms/overview/unit/nimwegen/) (Basel)

In my research, I combine quantitative experiments and theoretical models to elucidate how robust properties observed in bacterial populations arise from the seemingly stochastic dynamics observed in individual cells. Because bacteria are small and the chemical reactions involved in gene expression are inherently stochastic, different individual bacteria display different properties – so called phenotypes – even when they are genetically identical and exposed to the same environment. My [projects](#projects) investigate the molecular mechanisms underlying this phenotypic variability, as well as its functional and evolutionary implications. 

In practice, I develop new tools to study bacteria with single-cell resolution, in particular using microfluidics and image analysis. In parallel, I implement and promote [reproducible practices](resources) for experimental research and data analysis, and rely as much as possible on open source tools.

Have overlapping interests? Want to learn more about these approaches? Please [contact me](#contact) to discuss current opportunities to work together. In particular, I always welcome applications from talented and enthusiastic students and postdocs.

{%- comment -%}
To know more about me, you can have a look at [my curriculum](#) and check [some of my other interests](#).
{%- endcomment -%}
{% endcapture %}


{% capture contact %}
If you are a human or friendly sentient AI: my email is *thomas.julou*, followed immediately by *@normalesup.org*

Thomas Julou  
Biozentrum – University of Basel  
Spitalstrasse 41  
4056 Basel  
Switzerland

<hr>

To visit us, the Biozentrum is easily accessible from Basel main station by bus 30 (stop on the left when exiting the station; direction Bad Bf, stop UKBB) and from the airport by bus 50 (stop Kanenfeldplatz). Our lab is located on the 8th floor, first "quadrant" of the Biozentrum (room 08.018).
{% endcapture %}


<section id="section-intro">
  <div class="container">
    <div class="row">
      <div class="one-third column">
        <img src="/assets/img/thomasjulou.jpg">
        <!-- <p class="img-credit">photo by G. Hofman</p> -->
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

      <div class="project">
        <h2>Past projects</h2>
          <p>Read more <a href="archive">here</a> on my past research projects…</p>  
      </div>

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
  src="https://www.google.com/maps/embed/v1/place?q=Biozentrum&key=AIzaSyBhmRrxYN0evi_9JniNSGhJ7NFYFOAZyOs" allowfullscreen></iframe> 
        <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d1378405.7892098576!2d6.459358450004041!3d47.56392017918194!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x4791b908135df8df%3A0x850b8df911af1a74!2sBiozentrum+der+Universit%C3%A4t+Basel!5e0!3m2!1sen!2sch!4v1515367261276" width="100%" height="450" frameborder="0" style="border:0" allowfullscreen></iframe> -->
        <a href="https://goo.gl/maps/Cx4k4WYMEAK2"><img src="/assets/img/bz-map.jpg" width="100%" alt="map"></a>
      </div>
    </div>
  </div>
</section>
