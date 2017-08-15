---
layout: single
title: "Publications related to the [Lift project](http://www.lift-project.org/)"
permalink: /publications-lift/
author_profile: true
---

{% include base_path %}

{% for post in site.publications reversed  %}
  {% capture this_year %}{{ post.date | date: "%Y" }}{% endcapture %}
  {% capture next_year %}{{ post.previous.date | date: "%Y" }}{% endcapture %}

  {% if forloop.first %}
  <h3 id="{{ this_year }}-ref">{{this_year}}</h3>
  <ul>
  {% endif %}

{% if post.projects contains 'lift' %}
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
