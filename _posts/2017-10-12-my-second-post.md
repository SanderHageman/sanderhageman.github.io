---
layout: post
title: "My Second Post"
date: 2017-10-12
---


Second Post Test123
<br>
![My helpful screenshot]({{ "/assets/defaultThumb.jpg" | absolute_url }})
<br>
  {% for slide in site.slides %}
  slide.path
  {% endfor %}
{% include slides.html slide="my-pics1" %}
