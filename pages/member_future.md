---
layout: page
title: Members
subtitle:
permalink: "member_future"
---
{% comment %} Generated from _data/members.yml — add/move people there, not here. 3 cards per row; Alumni 5 per row with smaller pictures. {% endcomment %}
<style>
.member-small .col { padding-left: 6px; padding-right: 6px; }
.member-small { margin-bottom: 1.2rem; }
.member-small img { width: 100%; max-width: 110px; height: auto; }
.member-small h4 { font-size: 0.85rem; margin-bottom: 0.2rem; }
.member-small .col { font-size: 0.85rem; }
@media (max-width: 500px) { .member-small h4, .member-small .col { font-size: 0.7rem; } }
</style>
<div class="container-fluid">
{% for sec in site.data.members.sections %}
  {% assign ms = site.data.members.members | where: "section", sec.id %}
  {% if ms.size > 0 %}
  <h3>{{ sec.title }}</h3>
  <hr/>
  {% assign n = 3 %}{% assign small = "" %}
  {% if sec.id == "alumni" %}{% assign n = 5 %}{% assign small = " member-small" %}{% endif %}
  {% assign last_i = n | minus: 1 %}
  {% for m in ms %}
    {% assign i = forloop.index0 | modulo: n %}
    {% if i == 0 %}<div class="row{{ small }}">{% endif %}
    <div class="col no-gutters col-sm col-md">
      <div class="hovereffect">
        {% if m.page %}<a class="info" href="{{ m.page }}"><img class="img-responsive" src="/assets/img/people/{{ m.img }}" alt="{{ m.name }}"></a>{% else %}<img class="img-responsive" src="/assets/img/people/{{ m.img }}" alt="{{ m.name }}">{% endif %}
      </div><br>
      <h4>{{ m.role }}{% if m.years %}, {{ m.years }}{% endif %}</h4>
      {% if m.page %}<a href="{{ m.page }}">{{ m.name }}</a>{% else %}{{ m.name }}{% endif %}<br>
    </div>
    {% if forloop.last and i < last_i %}
      {% assign next_i = i | plus: 1 %}
      {% for k in (next_i..last_i) %}<div class="col no-gutters col-sm col-md"></div>{% endfor %}
    {% endif %}
    {% if i == last_i or forloop.last %}</div>{% endif %}
  {% endfor %}
  <br>
  {% endif %}
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
