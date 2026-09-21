---
layout: page
title: Media coverage
permalink: "media"
---
{% comment %} Entries live in _data/media.yml — edit that file, not this page. Newest first. {% endcomment %}
<style>
.media-embed { position: relative; width: 100%; padding-bottom: 56.25%; height: 0; margin: 10px 0 30px; }
.media-embed iframe { position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 0; }
</style>
{% assign years = site.data.media | map: "year" | uniq %}
{% for y in years %}
## {{ y }}
<hr>
{% assign items = site.data.media | where: "year", y %}
{% for m in items %}
<p><strong>{{ m.title }}</strong><br>
{{ m.outlet }} · {{ m.date }}{% if m.clip %} · clip {{ m.clip }}{% endif %}
· <a href="https://www.youtube.com/watch?v={{ m.youtube }}{% if m.start %}&t={{ m.start }}s{% endif %}" target="_blank">Watch on YouTube</a></p>
<div class="media-embed">
<iframe src="https://www.youtube-nocookie.com/embed/{{ m.youtube }}?rel=0{% if m.start %}&start={{ m.start }}{% endif %}{% if m.end %}&end={{ m.end }}{% endif %}" title="{{ m.title | escape }}" loading="lazy" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</div>
{% endfor %}
{% endfor %}
