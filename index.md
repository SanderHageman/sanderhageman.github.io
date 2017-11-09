---
layout: default
title: Sander Hageman; Portfolio website
---
# Portfolio Sander Hageman
## Student Games Programmer
Link to portfolio <a href="/portfolio">here</a>

## This is where I'll list the projects that should be instantly seen:
<div class="BestAchievements">
	<ul class="posts">
	 {% for project in site.projects %}
		{% if project.achievement %}
			<li>		
				<a href="{{ project.url }}" title="{{ project.title }}">
					{{ project.title }}
				</a>
				<br>
				{{ project.subtitle }}
			</li>
		{% endif %}
	{% endfor %}
	</ul>
</div>
