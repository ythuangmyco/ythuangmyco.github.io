---
layout: home
title: Welcome
show-avatar: true
subtitle: 黃尹則的個人研究網站<br> 
          Yin-Tse's research and personal page
cover-img: 
- assets/img/Marasmus_down.jpg
- assets/img/IMGP7709.jpg
- assets/img/Cnestus_mutilatus_donw.JPG
- assets/img/Scolytus_gallery_down.JPG
use-site-title: true
---
<div class="list-filters">
  <a href="/" class="list-filter filter-selected">All posts</a>
  <a href="/tags" class="list-filter">Index</a>
</div>

<div class="posts-list">
  {% for post in paginator.posts %}
  <article>
    <a class="post-preview" href="{{ post.url | prepend: site.baseurl }}">
	    <h2 class="post-title">{{ post.title }}</h2>
	
	    {% if post.subtitle %}
	    <h3 class="post-subtitle">
	      {{ post.subtitle }}
	    </h3>
	    {% endif %}
      <p class="post-meta">
        Posted on {{ post.date | date: "%B %-d, %Y" }}
      </p>

      <div class="post-entry">
        {{ post.content | truncatewords: 50 | strip_html | xml_escape}}
        <span href="{{ post.url | prepend: site.baseurl }}" class="post-read-more">[Read&nbsp;More]</span>
      </div>
    </a>  
   </article>
  {% endfor %}
</div>

{% if paginator.total_pages > 1 %}
<ul class="pager main-pager">
  {% if paginator.previous_page %}
  <li class="previous">
    <a href="{{ paginator.previous_page_path | prepend: site.baseurl | replace: '//', '/' }}">&larr; Newer Posts</a>
  </li>
  {% endif %}
  {% if paginator.next_page %}
  <li class="next">
    <a href="{{ paginator.next_page_path | prepend: site.baseurl | replace: '//', '/' }}">Older Posts &rarr;</a>
  </li>
  {% endif %}
</ul>
{% endif %}
