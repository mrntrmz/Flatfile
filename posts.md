---
title: Posts
layout: default
---

<ul>
{% for post in site.posts %}
  <li>
    <a href="{{ post.url }}">{{ post.title }}</a>
  </li>
{% endfor %}
</ul>

{% for post in site.posts %}
{{ post.content }}
{% endfor %}
