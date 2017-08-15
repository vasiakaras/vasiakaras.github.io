---
layout: single
title: "Publications by Project"
permalink: /publications-by-project/
author_profile: true
---

{% include base_path %}

{% assign projects =  site.publications | map: 'projects' | join: ','  | split: ',' | uniq %}
<!-- {% for project in projects %}
  <h2>{{ project }}</h2>
  <ul>
  {% for post in site.publications reversed %}
    {% if post.projects contains project %}
    {{ post.title }}
    {% endif %}
  {% endfor %}
  </ul>
{% endfor %} -->

{% for project in projects %}
  <h2>{{ project }}</h2>
  <ul>
{% for post in site.publications reversed  %}
  {% capture this_year %}{{ post.date | date: "%Y" }}{% endcapture %}
  {% capture next_year %}{{ post.previous.date | date: "%Y" }}{% endcapture %}

  {% if forloop.first %}
  <h3 id="{{ this_year }}-ref">{{this_year}}</h3>
  <ul>
  {% endif %}

{% if post.projects contains project %} 
  {% include publication-item.html %}
{% endif %}

  {% if forloop.last %}
  </ul>
  {% else %}
  {% if this_year != next_year %}
  </ul>
  <h3 id="{{ next_year }}-ref">{{next_year}}</h3>
  <ul>
  {% endif %}
  {% endif %}
{% endfor %}
  </ul>
{% endfor %}
