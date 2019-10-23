---
layout: home
title: Lógica UR
---
Guías de curso de Lógica ECH.

{% for d in site.deduccion %}
  [{{ d.title }}]({{d.url}})
{% endfor %}
