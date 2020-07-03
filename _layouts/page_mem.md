---
layout: base
---

{% include header.html type="page" %}

<div class="container-md" role="main">
  <div class="row">
    <div class="col-sm-1 offset-sm-1 col-md-2 offset-md-2 col-xl-3 offset-xl-3 col-lg-4 offset-lg-4">
      {{ content }}
      {% include comments.html %}
    </div>
  </div>
</div>
