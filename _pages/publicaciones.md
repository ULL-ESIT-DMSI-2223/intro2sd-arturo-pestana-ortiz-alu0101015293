---
title: Publicaciones    
layout: collection
permalink: /publicaciones/
collection: publicaciones
entries_layout: grid
classes: wide
---

Sample document listing for the collection `_publicaciones`.

Imprime todas las publicaciones que hemos hecho:

{% for i in site.posts %}
- {{ i.title }}
{% endfor %}
