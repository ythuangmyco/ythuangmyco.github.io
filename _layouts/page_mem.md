---
layout: base
---

{% include header.html type="page" %}

<div class="container-md" role="main">
  <div class="row">
    <div class="col-sm-8 offset-sm-2 col-md-8 offset-md-2 col-xl-8 offset-xl-2 col-lg-8 offset-lg-2">
      {{ content }}
      {% include comments.html %}
    </div>
  </div>
</div>
