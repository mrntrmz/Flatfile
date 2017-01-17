---
title: Cours
layout: page
---

<div>
{% for cours in site.cours %}
  <div class="cours">
    {{ cours.content }}
  </div>
{% endfor %}
</div>
