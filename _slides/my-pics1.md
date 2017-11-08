---
layout: iframe
title: my-pics1
---
{% assign image_files = site.static_files | where: "image", true | where_exp: "test", 'test.path contains page.title' %}

{% for myimage in image_files %}
    <li data-src="{{ myimage.path }}"></li>
{% endfor %}
