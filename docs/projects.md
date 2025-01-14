---
layout: default
title: "Projects"
permalink: /projects/
---

# My Projects

Here’s a list of my projects:

{% for project in site.projects %}
- [{{ project.title }}]({{ project.url | relative_url }}): {{ project.description }}
{% endfor %}
