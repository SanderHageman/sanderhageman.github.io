---
layout: default
title: Portfolio
---
<h1>{{ page.title }}</h1>
{% for project in site.projects %}
<div class="post">
* <a href="{{ project.url }}" title="{{ project.title }}"> {{ project.title }} </a>
	* {{ project.subtitle }}
</div>
{% endfor %}
