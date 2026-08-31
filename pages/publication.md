---
layout: page
title: Publications
permalink: "publication"
---
{% comment %} Entries live in _data/publications.yml — edit that file, not this page. Numbered per year, newest first with the highest number on top. {% endcomment %}
{% assign years = site.data.publications | map: "year" | uniq %}
{% for y in years %}
## {{ y }}
<hr>
{% assign pubs = site.data.publications | where: "year", y %}
<ol reversed>
{% for p in pubs %}
<li markdown="span">{{ p.citation }}{% if p.url %} [{{ p.url }}]({{ p.url }}){:target="_blank"}{% endif %}</li>
{% endfor %}
</ol>
{% endfor %}
