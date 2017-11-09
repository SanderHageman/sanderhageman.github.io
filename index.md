---
layout: default
title: Sander Hageman; Portfolio website
---
## Portfolio Sander Hageman
### Student Games Programmer
Link to portfolio <a href="/portfolio">here</a>

### Highlighted:
<div class="BestAchievements">
	<ul class="posts">
{% assign achievements = site.projects | where: "achievement", true %}
	 {% for project in achievements %} 
		
			<li>		
				<a href="{{ project.url }}" title="{{ project.title }}">
					{{ project.title }}
				</a>
				
				 {{ project.subtitle }}
			</li>
		
	{% endfor %}
	</ul>
</div>