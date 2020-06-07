---
layout: single
title: "Publications"
permalink: /publications/
author_profile: true
---
{% include base_path %}

{% if site.author.googlescholar or site.author.dblp %} 
You can also find my publications on my <a href="{{site.author.researchgate}}">ResearchGate</a> and <a href="{{site.author.googlescholar}}">Google Scholar</a> profile.
{% endif %}


{% include publication_types %}
<h3>Publication Type</h3>
<ul style="padding-left: 2em;">
{% for type in types  %}
  {% if type == '' %}
    {% continue %}
  {% endif %}
<li style="margin-bottom: 0em;"><strong><a href="#{{type | downcase | replace:' ','-'}}">{{type}}{% if type != 'Thesis' %}s{% endif %}</a></strong></li>
{% endfor %}
</ul>

{% include publications_list_by_type %}