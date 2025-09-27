---
layout: default
title: Home
---
## Velkommen til Blender Basics!

Her finder du forklaringer af de forskellige funktioner i Blender, samt forskellige opgaver hvor man kan bruge de enkelte værktøjer.

Hvis du ikke allerede har installeret Blender, så du klikke på [dette link](https://www.blender.org/download/) for at downloade det.

Hvis du gerne vil starte på opgaverne, så klik på [Opgave 1 - Det vigtigste](./_guides/01-getting-started.md)

Version 4

{% if site.guides.size > 0 %}

Line26added

  +  

<ul>

Line27added

  +  

{% for guide in site.guides %}

Line28added

  +  

<li><a href="{{ guide.url | relative_url }}">{{ guide.title }}</a></li>

Line29added

  +  

{% endfor %}

Line30added

  +  

</ul>

Line31added

  +  

{% else %}

Line32added

  +  

<p>Guides are coming soon!</p>

Line33added

  +  

{% endif %}