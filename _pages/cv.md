---
layout: archive
title: "Curriculum Vitae"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

Dr. Michel Steuwer

Professional Experience
------
* since August 2017: __Lecturer (Assistant Professor)__, _University of Glasgow_, UK.
* 2014 - 2017: __Postdoctoral Research Associate__, _The University of Edinburgh_, UK.
* 2010 - 2014: __Research Assosiate__, _University of Münster_, Germany.

Education
------
* __Ph.D in Computer Science__, _University of Münster_, Germany
  * Supervisor: Prof. Sergei Gorlatch
  * Thesis: _Improving Programmability and Performance Portability on Many-Core Processors_
  * Awarded with the highest possible grade: __Summa Cum Laude__ (_with highest honor_) 
  * Nominated as one of 34 candidates from all German, Austrian, and Swiss Universities for the __prize for best dissertation__ awarded by the German Informatics Society.
* __Diploma in Computer Science with a minor in Mathematics__, _University of Münster_, Germany
  * Thesis: _SkelCL — A Portable Multi-GPU Skeleton Library_
  * Overall grade in computer science: very good (85 %)

Publications
------
  <ul>{% for post in site.publications reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
  
Talks
------
  <ul>{% for post in site.talks reversed %}
    {% include archive-single-talk-cv.html %}
  {% endfor %}</ul>
  
<!-- Teaching
------
  <ul>{% for post in site.teaching %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul> -->
