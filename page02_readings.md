---
layout: page
title: Readings
img: barcelona.jpg
permalink: readings
caption: "Satellite view of Barcelona, Spain"
sidebar: true
---

---

<!--
This page autogenerates a list of readings by day and a collated list of links. 
All information is scraped from the _data/readings.yaml and _data/links.yaml.
Edit those to update the website
-->

Throughout the course, we will post readings mentioned in class or those that
we think are aligned with our scientific interests. NOTE: Though many of our
links will be to the original source literature, I will also draw liberally
from the tremendous work of science journalists such as David Quammen, Carl
Zimmer and Ed Yong. I have followed all of them closely and when they write
about areas I am close to, they almost always have it right, though of course
they express a point of view.

# Readings 

{% for day in site.data.readings %}
## {{day[0]}}
{% for pub in day[1] %}
* [**{{pub.title}}**]({% if pub.link_type == 'external' %}{{pub.link}}{%else%}{{site.baseurl}}/assets/pdfs/{{pub.link}}{%endif%}) by
  <i>{{pub.authors}}</i> ({{pub.year}}) {%if pub.description
  %}{{pub.description}}{%endif%}
{%endfor%}
{%endfor%}


# Videos
{% for day in site.data.videos %}
## {{day[0]}}
{% for video in day[1] %}
* [**{{video.title}}**]({{video.link}}) by
  <i>{{video.authors}}</i> ({{video.year}}). {%if video.description %}{{video.description}}{%endif%}
{%endfor%}
{%endfor%}




<center>
<h1> Useful links</h1>
</center>

---

{%for link in site.data.links%}
* [**{{link.title}}**]({{link.address}}) {%if link.description %}{{link.description}}{%endif%}
{%endfor%}

