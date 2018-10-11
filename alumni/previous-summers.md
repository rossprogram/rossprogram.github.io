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
{% if year.number_theory %}
<h3>Number theory</h3>
<dl>
<dt>Lecture</dt>
<dd>{{ year.number_theory.lecture }}</dd>
<dt>Seminars</dt>
<dd>{{ year.number_theory.seminars }}</dd>
</dl>
{% endif %}
{% if year.algebra_seminar %}
<h3>Algebra Seminar</h3>
<p>{{ year.algebra_seminar }}</p>
{% endif %}
{% if year.advanced_courses %}
<h3>Advanced courses</h3>
<dl>
{% for course in year.advanced_courses %}
<dt>{{ course[0] }}</dt>
<dd>{{ course[1] }}</dd>
{% endfor %}
</dl>
{% endif %}
{% if year.counselor_courses %}
<h3>Counselor courses</h3>
<dl>
{% for course in year.counselor_courses %}
<dt>{{ course[0] }}</dt>
<dd>{{ course[1] }}</dd>
{% endfor %}
</dl>
{% endif %}
{% if year.short_courses %}
<h3>Short courses</h3>
<dl>
{% for course in year.short_courses %}
<dt>{{ course[0] }}</dt>
<dd>{{ course[1] }}</dd>
{% endfor %}
</dl>
{% endif %}
{% if year.special_lectures %}
<h3>Special lectures</h3>
<p>{{ year.special_lectures }}</p>
{% endif %}
{% if year.conference %}
<h3>Special lectures</h3>
<p>{{ year.conference }}</p>
{% endif %}
{% endif %}
{% endfor %}

