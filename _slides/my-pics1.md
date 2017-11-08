---
layout: iframe
title: my-pics1
---
{% assign image_files = site.static_files | where: "image", true %}
{% for myimage in image_files %}
  {% if myimage.path contains "title" %}
    <li data-src="{{ myimage.path }}"></li>
  {% endif %}
{% endfor %}
