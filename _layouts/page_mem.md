---
layout: base
---

{% include header.html type="page" %}

<div class="container-md" role="main">
  <div class="row">
    <div class="col-sm-9 offset-sm-1.5 col-md-9 offset-md-1.5 col-xl-9 offset-xl-1.5 col-lg-9 offset-lg-1.5">
      {{ content }}
      {% include comments.html %}
    </div>
  </div>
</div>
