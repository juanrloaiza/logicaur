---
layout: content
title: Todos los ejercicios
ejercicios:
  - deduccion1
  - deduccion2
  - deduccion3
  - deduccion4
  - deduccion5
  - deduccion6
  - deduccion7
  - deduccion8
  - deduccion9
---
<div class="row">

{% assign counter = 1 %}
{% for string in page.ejercicios %}


  {% for ejercicio in site.data[string].ejercicios %}



  {% assign nombre = ejercicio.objetivo  | replace: "<->", "↔" | replace: "->", "→" | replace: ":existe:", "∃" | replace: ":todo:", "∀" %}

  <div class="deduccion col-lg-4 col-md-6">
    <div class="nombre">
      <span class="numero">{{ counter }}</span>)&nbsp;
        {% assign counter = counter | plus: 1 %}
      {{ nombre | replace: "<->", "↔" | replace: "->", "→" | replace: ":existe:", "∃" | replace: ":todo:", "∀" }}
    </div>



    {% if ejercicio.conjunto %}
    {{ ejercicio.conjunto  | replace: "<->", "↔" | replace: "->", "→" | replace: ":existe:", "∃" | replace: ":todo:", "∀" }}
    {% else %}

    {% assign premisas = ejercicio.premisas %}
    {% assign conclusiones = ejercicio.conclusiones %}


    {% include deduccion.html %}



  {% endif %}


  </div>


{% endfor %}


{% endfor %}
<div class="row">
