---
layout: default
title: Portfolio
---
# {{ page.title }}

<div id="portfolioList">
{% for project in site.projects %}
{% include projectItem.md proj=project %}
{% endfor %}
</div>	