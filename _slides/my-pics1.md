---
layout: iframe
title: my-pics1
---
{% assign image_files = site.static_files | where: "image", true | where_exp: "myimage", "myimage.path contains 'my-pics1'" %}
{% for myimage in image_files %}
    <li data-src="{{ myimage.path }}"></li>
{% endfor %}
