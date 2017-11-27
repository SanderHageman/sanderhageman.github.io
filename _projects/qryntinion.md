---
layout: post
title: "Qryntinion"
subtitle: "C++ Game engine with Playstation 4 and PC compatibility."
info: "Engine created by another student (Nicky van de Groep) which the team and I were contributing to. Purely C++ engine with ability to build the game for PS4 and PC using custom build tools."
date: 2015-11-01
projectDate: "November 2015 - February 2016"
---
{% include ytvideo.html id="-o2ILuoQrZE" %}
## Description
{{ page.info }}

## My Contributions
* __View frustum culling__
  * In this project I had to implement a basic form of view frustum culling. This was entirely cpu-based culling.
* __Sphere-based clustring__
  * To achieve a better performance in checking the models for collision with the frustum I implemented clusters for the models which were checked against.