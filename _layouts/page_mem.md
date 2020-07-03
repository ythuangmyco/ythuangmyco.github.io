---
layout: base
---

{% include header.html type="page" %}

<div class="container-md" role="main">
  <div class="row">
    <div class="col-sm-2 offset-sm-3 col-md-2 offset-md-3 col-xl-2 offset-xl-3 col-lg-2 offset-lg-3">
      {{ content }}
      {% include comments.html %}
    </div>
  </div>
</div>
