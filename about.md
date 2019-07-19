---
layout: default
title: About
---
# {{ page.title }}

Hello there, I am Sander Hageman,
Currently employed at Paladin Studios and creating amazing games. Before joining this company I was a student at Breda University of Applied Sciences (formerly known as NHTV) in Breda.
My first hands-on experience with creating games was when I was introduced to GameMaker at the age of 10, and I haven't stopped since. In 2014 I joined the ranks at the NHTV to study International Game Architecture and Design (IGAD) to learn more about making games. There I learned how to develop quality games at a high standard with large teams working closely together.


In my free time I like to play Pathfinder with my friends, play video games, listen to music and tinker with my linux server. I also love to participate in game jams like the Ludum Dare and the Global Game Jam and have developed lots of different games over the years.

{% capture programminglanguages-raw %}
* __Programming Languages__
  * C# (4 Years)
  * C++ (3 Years)
{% endcapture %}

{% capture engines-raw %}
* __Engines__
  * Unity (4, 5, 2017, -18)
  * Unreal Engine 4
{% endcapture %}

{% capture platforms-raw %}
* __Familiar development platforms__
  * PC
  * Android, iOS
  * PS4
{% endcapture %}

{% capture versioncontrol-raw %}
* __Version Control__
  * Git
  * Perforce
  * SVN
{% endcapture %}
  
{% capture programmingexperience-raw %}
* __Programming Experience__
  * Gameplay Programming
  * Engine(/graphics) Programming
  * AI Programming (NodeCanvas)
  * Virtual Reality
{% endcapture %}
  
{% capture spokenlanguages-raw %}
* __Spoken Languages__
  * Dutch (Native)
  * English (C2 / CPE)
{% endcapture %}

{% assign programminglanguages = programminglanguages-raw | markdownify %}
{% assign engines = engines-raw | markdownify %}
{% assign platforms = platforms-raw | markdownify %}
{% assign versioncontrol = versioncontrol-raw | markdownify %}
{% assign programmingexperience = programmingexperience-raw | markdownify %}
{% assign spokenlanguages = spokenlanguages-raw | markdownify %}

## Skills
<table class="skillstable">

  <tbody id="big">
    <tr>
      <td>{{ programminglanguages }}</td>
      <td>{{ platforms }}</td>
      <td>{{ versioncontrol }}</td>
    </tr>
    
    <tr>
      <td>{{ engines }}</td>
      <td>{{ programmingexperience }}</td>
      <td>{{ spokenlanguages }}</td>
    </tr>
  </tbody>
  
  <tbody id="small">
    <tr>
      <td>{{ programminglanguages }}</td>
      <td>{{ programmingexperience }}</td>
    </tr>
    
    <tr>
      <td>{{ engines }}</td>
      <td>{{ versioncontrol }}</td>
    </tr>
    
    <tr>
      <td>{{ platforms }}</td>
      <td>{{ spokenlanguages }}</td>
    </tr>
 </tbody>
  
</table>

* __Additional Skills__
  * Basics of HTML, CSS, Markdown and [Jekyll](https://jekyllrb.com/) by making this website.
  * The source can be found on [GitHub](https://github.com/sander12101/sander12101.github.io) where it is also hosted.
