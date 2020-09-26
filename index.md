--- 
layout: default 
title: Sander Hageman; Portfolio website
---
# Sander Hageman 
Game Programmer
<p class="pageSubtitle">
Dutch Game Programmer creating amazing games that make you smile at <a href="https://paladinstudios.com/">Paladin Studios</a>.
</p>

### Highlights:
<div id="portfolioList">
{% assign achievements = site.projects | where: "achievement", true | sort: 'date' %} 
{% for project in achievements reversed %}
	{% include projectItem.md proj=project %}
{% endfor %}
</div> <!-- portfolioList -->
