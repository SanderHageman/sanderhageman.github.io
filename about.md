---
layout: default
title: About
skills:
  - name: Programming Languages
    values:
      - C++ (3 Years)
      - C# (2 Years)
  - name: Engines
    values:
      - Unreal Engine 4
      - Unity 4, 5
---
# {{ page.title }}

Hello there, I am Sander Hageman, <br>
Currently I am a fourth year game programming student at the NHTV in Breda. I started programming when I was about 10 years old using Game Maker. In 2014 I went to the NHTV to study International Game Architecture and Design to learn more about making games. At the NHTV I learned about AAA game development and how to work in teams in varying sizes up to 30 people.

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
  * Git
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
  * English (Near Native)
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

* __Additional__
  * Basics of HTML, CSS, and [Jekyll](https://jekyllrb.com/) by making this website
  * source can be found on [GitHub](https://github.com/sander12101/sander12101.github.io) where it is also hosted
