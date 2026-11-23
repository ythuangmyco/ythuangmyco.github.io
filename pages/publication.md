---
layout: page
title: Publications
permalink: "publication"
---
{% comment %} Entries live in _data/publications.yml — edit that file, not this page. Numbered per year, newest first with the highest number on top. {% endcomment %}
<style>
.pub-list li { clear: both; margin-bottom: 0.9rem; }
.pub-list li.has-thumb { min-height: 5rem; }
.pub-thumb { float: right; width: 5rem; height: 5rem; object-fit: cover; border-radius: 0.5rem; border: 1px solid #ddd; background: #fff; margin: 0.2rem 0 0.4rem 1rem; }
@media (max-width: 500px) { .pub-thumb { width: 3.75rem; height: 3.75rem; } .pub-list li.has-thumb { min-height: 3.75rem; } }
</style>
<p style="font-size:0.9em; color:#6c757d; text-align:right; margin:0 0 -1.5rem 0;"><strong>#</strong> Corresponding author</p>
{% assign years = site.data.publications | map: "year" | uniq %}
{% for y in years %}
## {{ y }}
<hr>
{% assign pubs = site.data.publications | where: "year", y %}
<ol reversed class="pub-list">
{% for p in pubs %}
<li markdown="span"{% if p.thumb %} class="has-thumb"{% endif %}>{% if p.thumb %}<a href="{{ p.url | default: p.thumb }}" target="_blank"><img class="pub-thumb" src="{{ p.thumb | relative_url }}" alt="" loading="lazy"></a>{% endif %}{{ p.citation }}{% if p.url %} [{{ p.url }}]({{ p.url }}){:target="_blank"}{% endif %}</li>
{% endfor %}
</ol>
{% endfor %}
