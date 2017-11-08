---
layout: iframe
title: my-pics1
---

{% assign image_files = site.static_files %}
{% for myimage in image_files %}
Image:
  {{ myimage.path }}
{% endfor %}

* ![A nice pic of mine](my-pics1/pic1.jpg)
* ![Another nice pic of mine](my-pics1/pic2.jpg)
* ![Another nice pic of mine](my-pics1/pic3.jpg)
* ![Another nice pic of mine](my-pics1/pic4.jpg)
