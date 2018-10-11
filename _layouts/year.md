---
layout: single
---

{% if page.group_photo %}

{% capture fig_img %}
[![{{ page.year }}](/{{ page.group_photo }})](/{{ page.photo_key }})
{% endcapture %}

{% capture fig_caption %}
Group Photo, {{page.year}} Ross Program [with key](/{{ page.photo_key }})
{% endcapture %}

<figure>
  {{ fig_img | markdownify | remove: "<p>" | remove: "</p>" }}
  <figcaption>{{ fig_caption | markdownify | remove: "<p>" | remove: "</p>" }}</figcaption>
</figure>
{% else %}
  {{ content }}
{% endif %}

{% assign year = page %}
{% if year.number_theory or year.algebra_seminar or year.advanced_courses or year.counselor_courses or year.short_courses or year.special_lectures %}
{% include staff.html %}
{% endif %}
