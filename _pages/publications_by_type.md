---
layout: single
title: "Publications Organised by Type"
permalink: /publications-by-type/
author_profile: true
---
{% include base_path %}

{% assign types =  "Journal Article, Conference Paper, Workshop Paper, Book Chapter, Thesis, Technical Report" | split: ", " %}

 {% if site.author.googlescholar or site.author.dblp %} 
  You can also find my publications on {% if site.author.dblp %} <a href="{{site.author.dblp}}">my dblp profile</a> {% endif %} {% if site.author.googlescholar and site.author.dblp %} and {% endif %} {% if site.author.googlescholar %} <a href="{{site.author.googlescholar}}">my Google Scholar profile</a>{% endif %}.
 {% endif %} 

You find my publications also [organised by publication date](/publications/) and [organised by project](/publications-by-project/).

<h3>Publication Type</h3>
<ul style="padding-left: 2em;">
{% for type in types  %}
  {% if type == '' %}
    {% continue %}
  {% endif %}
<li style="margin-bottom: 0em;"><strong><a href="#{{type | downcase | replace:' ','-'}}">{{type}}{% if type != 'Thesis' %}s{% endif %}</a></strong></li>
{% endfor %}
</ul>

{% for type in types %}
  {% if type == '' %}
    {% continue %}
  {% endif %}
  <h2 id="{{type | downcase | replace:' ','-'}}">{{type}}{% if type != 'Thesis' %}s{% endif %}</h2>
  <ul>

{% assign last_year = '' %}
{% assign need_to_close_ul = false %}

{% for post in site.publications reversed  %}
{% if post.type contains type %}
  {% capture year %}{{ post.date | date: "%Y" }}{% endcapture %}
  {% if year != last_year %}
    {% if last_year != '' %}
</ul>
    {% endif %}
<h3 id="{{ year }}-ref">{{year}}</h3>
<ul>
  {% assign need_to_close_ul = true %}
  {% capture last_year %}{{year}}{% endcapture %}
  {% endif %}

  {% include publication-item.html %}
{% endif %}
{% endfor %}

{%if need_to_close_ul %}
</ul>
{% endif %}

  </ul>
{% endfor %}
