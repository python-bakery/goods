---
layout: default
title: Home
---

# 🐍 Python Bakery GOODS

Welcome to the GOODS collection of Python programs. Browse through the curated gallery below:

{% for program in site.pages %}
  {% if program.path contains 'gallery/' and program.name == 'README.md' %}
- [{{ program.title | default: program.dir | split: '/' | last }}]({{ program.url }})
  {% endif %}
{% endfor %}
