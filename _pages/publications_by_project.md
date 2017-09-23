---
layout: single
title: "Publications organised by research project"
permalink: /publications-by-project/
author_profile: true
---
{% include base_path %}

{% assign projects =  site.publications | map: 'projects' | join: ','  | split: ',' | uniq | sort %}

 {% if site.author.googlescholar or site.author.dblp %} 
  You can also find my publications on {% if site.author.dblp %} <a href="{{site.author.dblp}}">my dblp profile</a> {% endif %} {% if site.author.googlescholar and site.author.dblp %} and {% endif %} {% if site.author.googlescholar %} <a href="{{site.author.googlescholar}}">my Google Scholar profile</a>{% endif %}.
 {% endif %} 

You find my publications also [organised by publication date](/publications/).

<h3>Research projects</h3>
<ul style="padding-left: 2em;">
{% for project in projects  %}
  {% if project == '' %}
    {% continue %}
  {% endif %}
<li style="margin-bottom: 0em;"><strong><a href="#{{project | downcase | replace:' ','-'}}">{{project}}</a></strong></li>
{% endfor %}
</ul>

{% for project in projects %}
  {% if project == '' %}
    {% continue %}
  {% endif %}
  <h2 id="{{project | downcase | replace:' ','-'}}">{{ project }}</h2>
  <ul>

{% assign last_year = '' %}
{% assign need_to_close_ul = false %}

{% for post in site.publications reversed  %}
{% if post.projects contains project %}
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
