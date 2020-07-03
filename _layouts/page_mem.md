---
layout: base
---

{% include header.html type="page" %}

<div class="container-md" role="main">
  <div class="row">
    <div class="col-sm-9 offset-sm-2 col-md-9 offset-md-2 col-xl-9 offset-xl-2 col-lg-9 offset-lg-2">
      {{ content }}
      {% include comments.html %}
    </div>
  </div>
</div>
