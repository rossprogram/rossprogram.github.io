---
layout: single
title: Previous Summers
type: page
---

The following is a list of the Courses and Instructors, during the past several summer sessions.

{% assign sorted = site.years | reverse %}
{% for year in sorted %}
{% if year.number_theory or year.algebra_seminar or year.advanced_courses or year.counselor_courses or year.short_courses or year.special_lectures %}
<hr>
<h2>{{year.name}}</h2>
{% include staff.html %}
{% endif %}
{% endfor %}
