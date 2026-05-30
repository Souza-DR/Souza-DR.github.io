---
layout: page
permalink: /repositories/
title: repositories
description: Scientific software and code repositories related to my research.
nav: true
nav_order: 4
---

{% for group in site.data.repositories.repository_groups %}

## {{ group.title }}

{% if group.description %}
{{ group.description | markdownify }}
{% endif %}

{% if group.people %}

<p>
  <strong>{{ group.people_label }}:</strong>
  {% for person in group.people -%}
    <a href="{{ person.url }}">{{ person.name }}</a>{% unless forloop.last %}, {% endunless %}
  {%- endfor %}
</p>
{% endif %}

{% for repo in group.repositories %}

<div class="pb-3 mb-3 border-bottom">
  <h3 class="h5 mb-1">
    {% if repo.url %}
      <a href="{{ repo.url }}">{{ repo.name }}</a>
    {% else %}
      {{ repo.name }}
    {% endif %}
  </h3>

{% if repo.summary %}

<p class="mb-1">{{ repo.summary }}</p>
{% endif %}

{% if repo.related_title %}

<p class="mb-1">
<strong>Related work:</strong>
<a href="{{ repo.related_url | relative_url }}">{{ repo.related_title }}</a>
</p>
{% endif %}

{% if repo.status %}

<p class="mb-0"><strong>Status:</strong> {{ repo.status }}</p>
{% endif %}

</div>
{% endfor %}

{% endfor %}
