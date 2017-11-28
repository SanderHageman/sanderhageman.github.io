--- 
layout: default 
title: Sander Hageman; Portfolio website
---
# Sander Hageman 
<p class="pageSubtitle">
Dutch game programming student following International Game Architecture and Design at the NHTV, Breda.
</p>

### Released:
<div class="steamEmbed">
<iframe src="http://store.steampowered.com/widget/674400/" frameborder="0" width="100%" height="190"></iframe>
</div>

### Highlighted:
<div id="portfolioList">
{% assign achievements = site.projects | where: "achievement", true | sort: 'date' %} 
{% for project in achievements reversed %}
	{% include projectItem.md proj=project %}
{% endfor %}
</div> <!-- portfolioList -->