---
layout: default
title: Portfolio
---
<h1>{{ page.title }}</h1>
<ul class="posts">

  {% for project in site.projects %}

	<li>
		<p>
		<a href="{{ project.url }}" title="{{ project.title }}">

			<!-- {% if post.thumbnail %}
				<img src= {{post.thumbnail}} style="width:64px;height:64px;">
			{% else %}
				<img src= "/assets/defaultThumb.jpg" style="width:64px;height:64px;"> 
			{% endif %} -->

			{{ project.title }}
		</a>

		<br>
		
			{% if project.subtitle %}
				{{ project.subtitle | remove: '<p>' | remove: '</p>' }}
			{% else %}
				{{ project.excerpt | strip_html | remove: '<p>' | remove: '</p>' }}
			{% endif %}
		</p>
	</li>

  {% endfor %}
</ul>
