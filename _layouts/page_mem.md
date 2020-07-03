---
layout: base
---

{% include header.html type="page" %}

<div class="container-md" role="main">
  <div class="row">
    <div class="col-sm-10 offset-sm-1 col-md-10 offset-md-1 col-xl-10 offset-xl-1 col-lg-10 offset-lg-1">
      {{ content }}
      {% include comments.html %}
    </div>
  </div>
</div>
