---
title: contact
layout: page
---

<ul>
{% for partners in site.data.partners %}
  <li>
    <a href="https://github.com/{{ partners.github }}">
      {{ partners.nom }}
    </a>
  </li>
{% endfor %}
</ul>

contactez moi
