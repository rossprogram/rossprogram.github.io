---
layout: single
title: Group Photos
type: page
---

<figure class="third {{ include.class }}">
  {% for year in site.years %}
    {% if year.url %}
      <a href=
        {% if year.url contains "://" %}
          "{{ year.url }}"
        {% else %}
          "{{ year.url | relative_url }}"
        {% endif %}
        {% if year.title %}title="{{ year.title }}"{% endif %}
      >
        <img src=
          {% if year.thumbnail contains "://" %}
            "{{ year.thumbnail }}"
          {% else %}
            "{{ year.thumbnail | relative_url }}"
          {% endif %}
          alt="{% if year.alt %}{{ year.alt }}{% endif %}">
      </a>
    {% else %}
      <img src=
        {% if year.thumbnail contains "://" %}
          "{{ year.thumbnail }}"
        {% else %}
          "{{ year.thumbnail | relative_url }}"
        {% endif %}
        alt="{% if year.alt %}{{ year.alt }}{% endif %}">
    {% endif %}
  {% endfor %}
</figure>