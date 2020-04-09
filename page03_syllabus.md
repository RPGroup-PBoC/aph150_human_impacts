---
layout: page
title: Syllabus
img: amazon.jpg
permalink: syllabus
caption: "The Amazon"
sidebar: true
---


<table>
<tr>
    <th><b>Date</b></th>
    <th><b>Week</b></th>
    <th><b>Topic</b></th>
    <th><b>Recorded Lecture</b></th>
</tr>
{% for day in site.data.syllabus %}
<tr>
    <td>{{day.date}}</td>
    <td>{{day.week}}</td>
    <td>{{day.topic}}</td>
    {% if day.slides %}
    <td><a href="{{day.slides}}">
    Download </a></td>
    {% else %}
    <td>  </td>
    {% endif %}
</tr>
{% endfor %}
</table>