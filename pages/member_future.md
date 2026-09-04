---
layout: page
title: Members
subtitle:
permalink: "member_future"
---
{% comment %} Generated from _data/members.yml — add/move people there, not here. Max 3 cards per row. {% endcomment %}
<div class="container-fluid">
{% for sec in site.data.members.sections %}
  {% assign ms = site.data.members.members | where: "section", sec.id %}
  <h3>{{ sec.title }}</h3>
  <hr/>
  {% for m in ms %}
    {% assign i = forloop.index0 | modulo: 3 %}
    {% if i == 0 %}<div class="row">{% endif %}
    <div class="col no-gutters col-sm col-md">
      <div class="hovereffect">
        {% if m.page %}<a class="info" href="{{ m.page }}"><img class="img-responsive" src="/assets/img/people/{{ m.img }}" alt="{{ m.name }}"></a>{% else %}<img class="img-responsive" src="/assets/img/people/{{ m.img }}" alt="{{ m.name }}">{% endif %}
      </div><br>
      <h4>{{ m.role }}{% if m.years %}, {{ m.years }}{% endif %}</h4>
      {% if m.page %}<a href="{{ m.page }}">{{ m.name }}</a>{% else %}{{ m.name }}{% endif %}<br>
    </div>
    {% if forloop.last %}
      {% if i == 0 %}<div class="col no-gutters col-sm col-md"></div><div class="col no-gutters col-sm col-md"></div>{% elsif i == 1 %}<div class="col no-gutters col-sm col-md"></div>{% endif %}
    {% endif %}
    {% if i == 2 or forloop.last %}</div>{% endif %}
  {% endfor %}
  <br>
{% endfor %}
  <hr/>
  <br>
  <div class="row">
    <div class="col no-gutters col-sm col-md">
      <div class="hovereffect">
        <a class="info" href="join_us"><img class="img-responsive" src="/assets/img/people/joinus_circle_200.png" alt="Join us"></a>
      </div><br>
      <h4> </h4>
      <a href="join_us"> </a><br>
    </div>
    <div class="col no-gutters col-sm col-md"></div>
    <div class="col no-gutters col-sm col-md"></div>
  </div>
</div>
