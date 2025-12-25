---
layout: default
title: Tags
---

# 🏷️ Tags

<ul>
{% assign tags = site.recettes | map: "tags" | compact | uniq | sort %}
{% for tag in tags %}
  <li>
    <a href="/tags/{{ tag | slugify }}/">#{{ tag }}</a>
  </li>
{% endfor %}
</ul>