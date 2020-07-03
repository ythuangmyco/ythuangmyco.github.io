---
layout: base
---

{% include header.html type="page" %}

<div class="container-md" role="main">
  <div class="row">
    <div class="col-sm offset-sm col-md offset-md col-xl offset-xl col-lg offset-lg">
      {{ content }}
      {% include comments.html %}
    </div>
  </div>
</div>
