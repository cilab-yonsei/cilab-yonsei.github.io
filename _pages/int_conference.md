---
title: "CILAB - International Conference"
layout: gridlay
excerpt: "CILAB -- International Conference."
sitemap: false
permalink: /int_conference/
---

# International Conference

{% assign last_year = site.data.year_information.current_year %}
{% assign first_year = site.data.year_information.pub_first_showing_year %}

Jump to
{% for current_year in (first_year..last_year) reversed -%}
[{{ current_year }}](#{{ current_year }}),
{% endfor -%}
[Before {{ first_year }}](#before-{{ first_year }}).<br />

{% for current_year in (first_year..last_year) reversed %}
  {% assign data_exist = false %}
  {% for publi in site.data.publications.int_conference_list %}
    {% if publi.year == current_year %}
      {% assign data_exist = true %}
    {% endif %}
  {% endfor %}

  {% if data_exist %}
## {{ current_year }}
    {% for publi in site.data.publications.int_conference_list %}

      {% if publi.year == current_year %}

        {% if publi.vol_exist == 0 %}
          {% if publi.page_exist == 0 %}
<strong>{{ publi.title }}</strong> <br />
<em>{{ publi.authors }}</em> <br />
<em>{{ publi.conference }}</em>, {{ publi.venue }}, {{ publi.month }}, {{ publi.year }}.<br />
          {% endif %}
          {% if publi.page_exist == 1 %}
<strong>{{ publi.title }}</strong> <br />
<em>{{ publi.authors }}</em> <br />
<em>{{ publi.conference }}</em>, {{ publi.venue }}, {{ publi.month }}, {{ publi.year }}, no. {{ publi.page }}.<br />
          {% endif %}
        {% endif %}

        {% if publi.vol_exist == 1 %}
          {% if publi.page_exist == 0 %}
<strong>{{ publi.title }}</strong> <br />
<em>{{ publi.authors }}</em> <br />
<em>{{ publi.conference }}</em>, {{ publi.venue }}, {{ publi.month }}, {{ publi.year }}, vol. {{ publi.vol }}.<br />
          {% endif %}
          {% if publi.page_exist == 1 %}
<strong>{{ publi.title }}</strong> <br />
<em>{{ publi.authors }}</em> <br />
<em>{{ publi.conference }}</em>, {{ publi.venue }}, {{ publi.month }}, {{ publi.year }}, vol. {{ publi.vol }}, no. {{ publi.page }}.<br />
          {% endif %}
        {% endif %}

      {% endif %}
      
    {% endfor %}
  {% endif %}
{% endfor %}

## Before {{ first_year }}
{% for publi in site.data.publications.int_conference_list %}

  {% if publi.year < first_year %}

    {% if publi.vol_exist == 0 %}
      {% if publi.page_exist == 0 %}
<strong>{{ publi.title }}</strong> <br />
<em>{{ publi.authors }}</em> <br />
<em>{{ publi.conference }}</em>, {{ publi.venue }}, {{ publi.month }}, {{ publi.year }}.<br />
      {% endif %}
      {% if publi.page_exist == 1 %}
<strong>{{ publi.title }}</strong> <br />
<em>{{ publi.authors }}</em> <br />
<em>{{ publi.conference }}</em>, {{ publi.venue }}, {{ publi.month }}, {{ publi.year }}, no. {{ publi.page }}.<br />
      {% endif %}
    {% endif %}

    {% if publi.vol_exist == 1 %}
      {% if publi.page_exist == 0 %}
<strong>{{ publi.title }}</strong> <br />
<em>{{ publi.authors }}</em> <br />
<em>{{ publi.conference }}</em>, {{ publi.venue }}, {{ publi.month }}, {{ publi.year }}, vol. {{ publi.vol }}.<br />
      {% endif %}
      {% if publi.page_exist == 1 %}
<strong>{{ publi.title }}</strong> <br />
<em>{{ publi.authors }}</em> <br />
<em>{{ publi.conference }}</em>, {{ publi.venue }}, {{ publi.month }}, {{ publi.year }}, vol. {{ publi.vol }}, no. {{ publi.page }}.<br />
      {% endif %}
    {% endif %}
  {% endif %}

{% endfor %}