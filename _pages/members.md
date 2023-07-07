---
title: "CILAB - Members"
layout: gridlay
excerpt: "CILAB: Members"
sitemap: false
permalink: /members/
---

# Professor
{% assign number_printed = 0 %}
{% for member in site.data.members.professor %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: center" />
  <h4>{{ member.name }}</h4>
  <i>email: <{{ member.email }}></i>
  <ul style="overflow: hidden">
  </ul>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

# Students

Jump to [Master's/Doctoral Combined Program Students](#combined-students), [PhD Program Students](#phd-students) and [Master Program Students](#master-students) and [Undergraduate Students](#untergraduate-students).

## Master's/Doctoral Combined Program Students <a id="combined-students"></a>
{% assign number_printed = 0 %}
{% for member in site.data.members.students.combined_list %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

{% if member.cv.exist == 1 and member.homepage.exist == 1 %}
<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: center" />
  <h4>{{ member.name }}</h4>
  <i>email: <{{ member.email }}><br>research interest: {{ member.research }}</i>
  <br><i>link: </i><a href="{{ member.cv.url }}">[CV] </a>
  <a href="{{ member.homepage.url }}">[Homepage]</a>
  <ul style="overflow: hidden">
  </ul>
</div>
{% endif %}

{% if member.cv.exist == 1 and member.homepage.exist == 0 %}
<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: center" />
  <h4>{{ member.name }}</h4>
  <i>email: <{{ member.email }}><br>research interest: {{ member.research }}</i>
  <br><i>link: </i><a href="{{ member.cv.url }}">[CV] </a>
  <ul style="overflow: hidden">
  </ul>
</div>
{% endif %}


{% if member.cv.exist == 0 and member.homepage.exist == 1 %}
<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: center" />
  <h4>{{ member.name }}</h4>
  <i>email: <{{ member.email }}><br>research interest: {{ member.research }}</i>
  <br><i>link: </i><a href="{{ member.homepage.url }}">[Homepage]</a>
  <ul style="overflow: hidden">
  </ul>
</div>
{% endif %}

{% if member.cv.exist == 0 and member.homepage.exist == 0 %}
<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: center" />
  <h4>{{ member.name }}</h4>
  <i>email: <{{ member.email }}><br>research interest: {{ member.research }}</i>
  <br>
  <ul style="overflow: hidden">
  </ul>
</div>
{% endif %}

<!-- {% if member.research == nil and member.cv.exist == 1 %}
<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: center" />
  <h4>{{ member.name }}</h4>
  <i>email: <{{ member.email }}><br>Affiliation: {{ member.affiliation }}</i>
  <br>CV: <a href="{{ member.cv.url }}">download</a>
  <ul style="overflow: hidden">
  </ul>
</div>
{% endif %}

{% if member.research != nil and member.cv.exist == 1 %}
<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: center" />
  <h4>{{ member.name }}</h4>
  <i>email: <{{ member.email }}><br>research interest: {{ member.research }}</i>
  <br>CV: <a href="{{ member.cv.url }}">download</a>
  <ul style="overflow: hidden">
  </ul>
</div>
{% endif %}

{% if member.research == nil and member.cv.exist == 0 %}
<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: center" />
  <h4>{{ member.name }}</h4>
  <i>email: <{{ member.email }}><br>Affiliation: {{ member.affiliation }}</i>
  <br>
  <ul style="overflow: hidden">
  </ul>
</div>
{% endif %}

{% if member.research != nil and member.cv.exist == 0 %}
<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: center" />
  <h4>{{ member.name }}</h4>
  <i>email: <{{ member.email }}><br>research interest: {{ member.research }}</i>
  <br>
  <ul style="overflow: hidden">
  </ul>
</div>
{% endif %} -->


{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

## PhD Program Students <a id="phd-students"></a>
{% assign number_printed = 0 %}
{% for member in site.data.members.students.phd_list %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

{% if member.research == nil and member.cv.exist == 1 %}
<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: center" />
  <h4>{{ member.name }}</h4>
  <i>email: <{{ member.email }}><br>Affiliation: {{ member.affiliation }}</i>
  <br>CV: <a href="{{ member.cv.url }}">download</a>
  <ul style="overflow: hidden">
  </ul>
</div>
{% endif %}

{% if member.research != nil and member.cv.exist == 1 %}
<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: center" />
  <h4>{{ member.name }}</h4>
  <i>email: <{{ member.email }}><br>research interest: {{ member.research }}</i>
  <br>CV: <a href="{{ member.cv.url }}">download</a>
  <ul style="overflow: hidden">
  </ul>
</div>
{% endif %}

{% if member.research == nil and member.cv.exist == 0 %}
<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: center" />
  <h4>{{ member.name }}</h4>
  <i>email: <{{ member.email }}><br>Affiliation: {{ member.affiliation }}</i>
  <br>
  <ul style="overflow: hidden">
  </ul>
</div>
{% endif %}

{% if member.research != nil and member.cv.exist == 0 %}
<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: center" />
  <h4>{{ member.name }}</h4>
  <i>email: <{{ member.email }}><br>research interest: {{ member.research }}</i>
  <br>
  <ul style="overflow: hidden">
  </ul>
</div>
{% endif %}


{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

## Master Program Students <a id="master-students"></a>
{% assign number_printed = 0 %}
{% for member in site.data.members.students.ms_list %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

{% if member.research == nil and member.cv.exist == 1 %}
<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: center" />
  <h4>{{ member.name }}</h4>
  <i>email: <{{ member.email }}><br>Affiliation: {{ member.affiliation }}</i>
  <br>CV: <a href="{{ member.cv.url }}">download</a>
  <ul style="overflow: hidden">
  </ul>
</div>
{% endif %}

{% if member.research != nil and member.cv.exist == 1 %}
<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: center" />
  <h4>{{ member.name }}</h4>
  <i>email: <{{ member.email }}><br>research interest: {{ member.research }}</i>
  <br>CV: <a href="{{ member.cv.url }}">download</a>
  <ul style="overflow: hidden">
  </ul>
</div>
{% endif %}

{% if member.research == nil and member.cv.exist == 0 %}
<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: center" />
  <h4>{{ member.name }}</h4>
  <i>email: <{{ member.email }}><br>Affiliation: {{ member.affiliation }}</i>
  <br>
  <ul style="overflow: hidden">
  </ul>
</div>
{% endif %}

{% if member.research != nil and member.cv.exist == 0 %}
<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: center" />
  <h4>{{ member.name }}</h4>
  <i>email: <{{ member.email }}><br>research interest: {{ member.research }}</i>
  <br>
  <ul style="overflow: hidden">
  </ul>
</div>
{% endif %}

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}


## Undergraduate Students <a id="undergraduate-students"></a>
{% assign number_printed = 0 %}
{% for member in site.data.members.students.under_list %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

{% if member.research == nil and member.cv.exist == 1 %}
<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: center" />
  <h4>{{ member.name }}</h4>
  <i>email: <{{ member.email }}><br>Affiliation: {{ member.affiliation }}</i>
  <br>CV: <a href="{{ member.cv.url }}">download</a>
  <ul style="overflow: hidden">
  </ul>
</div>
{% endif %}

{% if member.research != nil and member.cv.exist == 1 %}
<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: center" />
  <h4>{{ member.name }}</h4>
  <i>email: <{{ member.email }}><br>research interest: {{ member.research }}</i>
  <br>CV: <a href="{{ member.cv.url }}">download</a>
  <ul style="overflow: hidden">
  </ul>
</div>
{% endif %}

{% if member.research == nil and member.cv.exist == 0 %}
<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: center" />
  <h4>{{ member.name }}</h4>
  <i>email: <{{ member.email }}><br>Affiliation: {{ member.affiliation }}</i>
  <br>
  <ul style="overflow: hidden">
  </ul>
</div>
{% endif %}

{% if member.research != nil and member.cv.exist == 0 %}
<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: center" />
  <h4>{{ member.name }}</h4>
  <i>email: <{{ member.email }}><br>research interest: {{ member.research }}</i>
  <br>
  <ul style="overflow: hidden">
  </ul>
</div>
{% endif %}


{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}