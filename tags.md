---
layout: default
title: Tags
---

# 🏷️ Tags
<ul>
{% assign all_tags = "" | split: "" %}

{% for recette in site.recettes %}
  {% for tag in recette.tags %}
    {% unless all_tags contains tag %}
      {% assign all_tags = all_tags | push: tag %}
    {% endunless %}
  {% endfor %}
{% endfor %}

{% assign all_tags = all_tags | sort %}

{% for tag in all_tags %}
  <li>
    <a href="{{ site.baseurl }}/tags/{{ tag | slugify }}/">#{{ tag }}</a>
  </li>
{% endfor %}
</ul>
