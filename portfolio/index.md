---
layout: default
title: Portfolio
---
# {{ page.title }}
{% for project in site.projects %}
* [{{ project.title }}]({{ project.url }})
	* {{ project.subtitle }}
{% endfor %}
