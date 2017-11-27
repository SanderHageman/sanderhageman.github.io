---
layout: default
title: Portfolio
---
# {{ page.title }}

<div id="portfolioList">
{% assign projectsSorted = site.projects | sort: 'date' %}
{% for project in projectsSorted reversed %}
{% include projectItem.md proj=project %}
{% endfor %}
</div>	