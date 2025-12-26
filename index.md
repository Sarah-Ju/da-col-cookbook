---
layout: default
title: Accueil
---

# 🍽️ Mes recettes

Bienvenue sur le site des recettes des Da Col. Il y a actuellement {{ site.recettes | size }} recettes sur le site. Bon appétit !

## Catégories
- [Soupes]({{ site.baseurl }}/categories/soupes/)
- [Entrées]({{ site.baseurl }}/categories/entrees/)
- [Plats]({{ site.baseurl }}/categories/plats/)
- [Desserts]({{ site.baseurl }}/categories/desserts/)


## Explorer
- [Par tags](/tags.md)

## Toutes les recettes
<ul>
{% for recette in site.recettes %}
  <li>
    <a href="{{site.baseurl }}{{ recette.url }}">{{ recette.title }}</a>
  </li>
{% endfor %}
</ul>