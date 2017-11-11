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
{% assign achievements = site.projects | where: "achievement", true %} 
{% for project in achievements %}
* [{{ project.title }}]({{ project.url }})
	* {{ project.subtitle }}
{% endfor %}