---
title: Instrucciones hospedadas en línea
permalink: index.html
layout: home
---

# Directorio de contenido

A continuación se enumeran hipervínculos a cada uno de los ejercicios de laboratorio y demostraciones.

## Laboratorios

{% assign labs = site.pages | where_exp:"page", "page.url contains '/Instructions'" %}
| Sección | Laboratorio |
| --- | --- | 
{% for activity in labs  %}| {{ activity.lab.module }} | [{{ activity.lab.title }}{% if activity.lab.type %} - {{ activity.lab.type }}{% endif %}]({{ site.github.url }}{{ activity.url }}) |
{% endfor %}
