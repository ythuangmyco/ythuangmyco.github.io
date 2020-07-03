---
layout: base
---

{% include header.html type="page" %}

<div class="container-md" role="main">
  <div class="row">
    <div class="col-sm-8 offset-sm-1 col-md-8 offset-md-1 col-xl-8 offset-xl-1 col-lg-8 offset-lg-1">
      {{ content }}
      {% include comments.html %}
    </div>
  </div>
</div>
