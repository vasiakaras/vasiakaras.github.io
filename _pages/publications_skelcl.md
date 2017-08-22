---
layout: single
title: "Publications related to the [SkelCL project](https://skelcl.github.io/)"
permalink: /publications-skelcl/
author_profile: true
---

{% include base_path %}

{% assign last_year = '' %}
{% assign need_to_close_ul = false %}

{% for post in site.publications reversed  %}
{% if post.projects contains 'SkelCL' %}
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
