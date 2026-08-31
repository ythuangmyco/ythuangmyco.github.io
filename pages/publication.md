---
layout: page
title: Publications
permalink: "publication"
---
{% comment %} Entries live in _data/publications.yml — edit that file, not this page. {% endcomment %}
{% assign years = site.data.publications | map: "year" | uniq %}
{% for y in years %}
## {{ y }}
<hr>
{% assign pubs = site.data.publications | where: "year", y %}
{% for p in pubs %}
{{ p.citation }}{% if p.url %} [{{ p.url }}]({{ p.url }}){:target="_blank"}{% endif %}<br>

{% endfor %}
{% endfor %}
