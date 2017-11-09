---
layout: default
title: Sander Hageman; Portfolio website
---
<div class="MainPageContent">
	<h1>Portfolio Sander Hageman</h1>
	<h2>Student Games Programmer</h2>
	<p>Link to portfolio <a href="/portfolio">here</a></p>
</div>

<div class="BestAchievements">
	##This is where I'll list the projects that should be instantly seen:
	
	 {% for post in site.posts %}
		{% if post.achievement %}
			<ul class="posts">
			<li>		
				<a href="{{ post.url }}" title="{{ post.title }}">
					{{ post.title }}
				</a>
			</li>
			</ul>
		{% endif %}
	{% endfor %}
</div>
