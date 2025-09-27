---
layout: default
title: Home
---

# Blender Basics

Welcome to the Blender Basics guide for use at Coding Pirates!

This site provides step-by-step tutorials and guides to help you learn the fundamentals of Blender, a powerful 3D creation software.

## Getting Started

- [What is Blender?](#what-is-blender)
- [Installation](#installation)
- [Basic Interface](#basic-interface)
- [Your First Model](#your-first-model)

## What is Blender?

Blender is a free and open-source 3D computer graphics software toolset used for creating animated films, visual effects, art, 3D printed models, motion graphics, interactive 3D applications, virtual reality, and computer games.

## Guides

{% if site.guides.size > 0 %}
<ul>
{% for guide in site.guides %}
  <li><a href="{{ guide.url | relative_url }}">{{ guide.title }}</a></li>
{% endfor %}
</ul>
{% else %}
<p>Guides are coming soon!</p>
{% endif %}

---

*This guide is maintained for Coding Pirates educational purposes.*