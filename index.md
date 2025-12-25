---
layout: default
title: Accueil
---

# 🍽️ Mes recettes

Bienvenue sur le site des recettes des Da Col. Il y a actuellement {{ site.recettes | size }} recettes sur le site. Bon appétit !

## Catégories
- [Soupes](#)
- [Desserts](#)

## Explorer
- [Par tags](/tags.md)

## Toutes les recettes
<ul>
{% for recette in site.recettes %}
    -[{{ recette.title }}]({{ recette.url }})
  <li>
    [{{ recette.title }}](/{{ recette.url }})<br>
    <a href="{{ recette.url }}">{{ recette.title }}</a>
  </li>
{% endfor %}
</ul>