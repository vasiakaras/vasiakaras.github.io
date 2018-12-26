---
layout: single
title: "People I work with"
permalink: /people/
redirect_from:
  - /team/
author_profile: true
---
{% assign people = site.people | group_by: 'type' | sort: 'start-year' %}

<h2>Students</h2>

{% include people-category name="PhD Students" %}
{% include people-category name="Co-Supervised PhD Students" %}
{% include people-category name="Former PhD Students" %}
{% include people-category name="Former Co-Supervised PhD Students" %}
