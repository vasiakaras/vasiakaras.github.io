---
layout: single
title: "People I work with"
permalink: /people/
redirect_from:
  - /team/
author_profile: true
---
{% assign people = site.people | sort: 'start-year' | group_by: 'type' %}

<h2>Students</h2>

{% include people-category name="PhD Students" %}
{% include people-category name="Co-Supervised PhD Students" %}
{% include people-category name="Former PhD Students" %}
{% include people-category name="Former Co-Supervised PhD Students" %}
