---
layout: home
title: Lógica UR
---
Autores: Fabio Fang...

Bienvenides al sitio del curso de Lógica ECH. Aquí encontrarán las guías para cada sección del curso.

## Deducción Natural
{% for d in site.deduccion %}
  [{{ d.title }}]({{ site.baseurl }}{{d.url}})
{% endfor %}
