---
layout: base
---

{% include header.html type="page" %}

<div class="container-md" role="main">
  <div class="row">
    <div class="col-sm-9 col-md-9 col-xl-9 col-lg-9">
      {{ content }}
      {% include comments.html %}
    </div>
  </div>
</div>
