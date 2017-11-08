---
layout: iframe
title: my-pics1
markdown: null
---
{% assign image_files = site.static_files | where: "image", true | where_exp: "myimage", 'myimage.path contains page.title' %}
{% for myimage in image_files %}
    <li data-src="{{ myimage.path }}"></li>
{% endfor %}
