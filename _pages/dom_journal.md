---
title: "CILAB - Domestic Journal"
layout: gridlay
excerpt: "CILAB -- Domestic Journal."
sitemap: false
permalink: /dom_journal/
---

# Domestic Journal

{% assign last_year = site.data.year_information.current_year %}
{% assign first_year = site.data.year_information.pub_first_showing_year %}

Jump to
{% for current_year in (first_year..last_year) reversed -%}
[{{ current_year }}](#{{ current_year }}),
{% endfor -%}
[Before {{ first_year }}](#before-{{ first_year }}).<br />

{% for current_year in (first_year..last_year) reversed %}
  {% assign data_exist = false %}
  {% for publi in site.data.publications.dom_journal_list %}
    {% if publi.year == current_year %}
      {% assign data_exist = true %}
    {% endif %}
  {% endfor %}

  {% if data_exist %}
## {{ current_year }}
    {% for publi in site.data.publications.dom_journal_list %}
      {% if publi.year == {{current_year}} %}

        {% if publi.accepted == 0 %}
<strong>{{ publi.title }}</strong> <br />
<em>{{ publi.authors }}</em> <br />
<em>{{ publi.journal }}</em>, vol. {{ publi.vol }}, no. {{ publi.issue }}, pp. {{ publi.page }}, {{ publi.month }}, {{ publi.year }}.<br />
        {% endif %}

        {% if publi.accepted == 1 %}
<strong>{{ publi.title }}</strong> <br />
<em>{{ publi.authors }}</em> <br />
<em>{{ publi.journal }}</em>,  {{ publi.year }}  {{ publi.description }}.<br />
        {% endif %}

      {% endif %}
    {% endfor %}
  {% endif %}
{% endfor %}

## Before {{ first_year }}
{% for publi in site.data.publications.dom_journal_list %}

  {% if publi.year < {{first_year}} %}

  {% if publi.accepted == 0 %}
  <strong>{{ publi.title }}</strong> <br />
  <em>{{ publi.authors }}</em> <br />
  <em>{{ publi.journal }}</em>, vol. {{ publi.vol }}, no. {{ publi.issue }}, pp. {{ publi.page }}, {{ publi.month }}, {{ publi.year }}.<br />
  {% endif %}

  {% if publi.accepted == 1 %}
  <strong>{{ publi.title }}</strong> <br />
  <em>{{ publi.authors }}</em> <br />
  <em>{{ publi.journal }}</em>,  {{ publi.year }}  {{ publi.description }}.<br />
  {% endif %}

  {% endif %}

{% endfor %}