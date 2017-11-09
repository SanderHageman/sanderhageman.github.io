---
layout: default
title: Portfolio
---
<h1>{{ page.title }}</h1>
<ul class="posts">

  {% for post in site.post %}

	<li>
		<p>
		<a href="{{ post.url }}" title="{{ post.title }}">

			<!-- {% if post.thumbnail %}
				<img src= {{post.thumbnail}} style="width:64px;height:64px;">
			{% else %}
				<img src= "/assets/defaultThumb.jpg" style="width:64px;height:64px;"> 
			{% endif %} -->

			{{ post.title }}
		</a>

		<br>
		
			{% if post.subtitle %}
				{{ post.subtitle | remove: '<p>' | remove: '</p>' }}
			{% else %}
				{{ post.excerpt | strip_html | remove: '<p>' | remove: '</p>' }}
			{% endif %}
		</p>
	</li>

  {% endfor %}
</ul>