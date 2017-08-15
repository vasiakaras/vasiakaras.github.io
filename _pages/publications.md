---
layout: single
title: "Publications"
permalink: /publications/
author_profile: true
---

 {% if site.author.googlescholar or site.author.dblp %} 
  You can also find my publications on {% if site.author.dblp %} <a href="{{site.author.dblp}}">my dblp profile</a> {% endif %} {% if site.author.googlescholar and site.author.dblp %} and {% endif %} {% if site.author.googlescholar %} <a href="{{site.author.googlescholar}}">my Google Scholar profile</a>{% endif %}.
 {% endif %} 

{% include base_path %}

{% for post in site.publications reversed  %}
  {% capture this_year %}{{ post.date | date: "%Y" }}{% endcapture %}
  {% capture next_year %}{{ post.previous.date | date: "%Y" }}{% endcapture %}

  {% if forloop.first %}
  <h2 id="{{ this_year }}-ref">{{this_year}}</h2>
  <ul class="publications">
  {% endif %}

  {% include publication-item.html %}

  {% if forloop.last %}
  </ul>
  {% else %}
  {% if this_year != next_year %}
  </ul>
  <h2 id="{{ next_year }}-ref">{{next_year}}</h2>
  <ul>
  {% endif %}
  {% endif %}
{% endfor %}
