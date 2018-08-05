---
layout: default
title: About
---
# {{ page.title }}

Hello there, I am Sander Hageman, <br>
Currently I am a fourth-year game programming student at the NHTV (Breda University) in Breda. I started programming when I was about 10 years old using Game Maker. In 2014 I went to the NHTV to study International Game Architecture and Design to learn more about making games. At the NHTV I learned about AAA game development and how to work in teams in varying sizes up to 30 people.


In my free time I like to play Pathfinder with my friends, play video games, listen to music and tinker with my linux server. I also love to participate in game jams like the Ludum Dare and the Global Game Jam and have developed lots of different games over the years.

{% capture programminglanguages-raw %}
* __Programming Languages__
  * C++ (3 Years)
  * C# (2 Years)
{% endcapture %}

{% capture engines-raw %}
* __Engines__
  * Unreal Engine 4
  * Unity 4, 5
{% endcapture %}

{% capture platforms-raw %}
* __Platforms__
  * PC
  * PS4
  * Android
{% endcapture %}

{% capture versioncontrol-raw %}
* __Version Control__
  * Perforce
  * SVN
{% endcapture %}
  
{% capture programmingexperience-raw %}
* __Programming Experience__
  * Gameplay Programming
  * Engine Programming
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
  * Basics of HTML, CSS, Git, and [Jekyll](https://jekyllrb.com/) by making this
  * website. The source can be found on [GitHub](https://github.com/sander12101/sander12101.github.io) where it is also hosted
