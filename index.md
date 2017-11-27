--- 
layout: default 
title: Sander Hageman; Portfolio website
---
# Sander Hageman 
<p class="pageSubtitle">
Game Programmer
</p>

### Released:
<div class="steamEmbed">
<iframe src="http://store.steampowered.com/widget/674400/" frameborder="0" width="100%" height="190"></iframe>
</div>

### Highlighted:
<div id="portfolioList">
{% assign achievements = site.projects | where: "achievement", true %} 
{% for project in achievements %}
{% include projectItem.md proj=project %}
{% comment %}
* [{{ project.title }}]({{ project.url }})
	* {{ project.subtitle }}
{% endcomment %}
{% endfor %}
</div> <!-- portfolioList -->