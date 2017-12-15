--- 
layout: default 
title: Sander Hageman; Portfolio website
---
# Sander Hageman 
Game Programmer
<p class="pageSubtitle">
Dutch game programming student following International Game Architecture and Design course at the NHTV, Breda.
</p>

### Highlights:
<div id="portfolioList">
{% assign achievements = site.projects | where: "achievement", true | sort: 'date' %} 
{% for project in achievements reversed %}
	{% include projectItem.md proj=project %}
{% endfor %}
</div> <!-- portfolioList -->