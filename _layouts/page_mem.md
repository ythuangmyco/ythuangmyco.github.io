---
layout: base
---

{% include header.html type="page" %}

<div class="container-md" role="main">
  <div class="row">
    <div class="col-sm-8 offset-sm-8 col-md-8 offset-md-8 col-xl-8 offset-xl-8 col-lg-8 offset-lg-8">
      {{ content }}
      {% include comments.html %}
    </div>
  </div>
</div>
