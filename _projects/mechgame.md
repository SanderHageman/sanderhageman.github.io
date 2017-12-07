---
layout: post
title: "Mech Game"
subtitle: "VR Mech simulation game made in Unity for the PC."
info: "In this game the player is the pilot of a ‘Mech’ fighting robot who has to protect themselves from the hordes of enemies that approach from all directions while also walking to beacons that have to be lit to complete the game."
date: 2016-01-02
projectDate: "January 2016 - April 2016"
role: Hardware Implementation
contributions:
  - name: Occulus Rift
    shortdesc: Adding support for Occulus Rift
    desc: Adding support for virtual reality in the game. This included seting it up to work with the Occulus Rift and making sure it worked correctly in the game.
  - name: Razor Hydra
    shortdesc: Adding support for Razor Hydra
    desc: Implementation of the Razor Hydra. This meant using the Razor Hydra API and integrating it into the game. At the time of development the Hydras had already been discontinued which made development a little harder.
  - name: Inverse Kinematics
    shortdesc: Implementation of IK
    desc: Because the player was free to move the hands of the Mech using the Razor Hydras I had to implement IK to make the arms of the mech react to the movements of the player as good as possible. This can be viewed [on youtube](https://www.youtube.com/watch?v=A-OfPg-s0TE).
---
{% include ytvideo.html id="Gth0KCI_A5g" %}

## Description
{{ page.info }} The player controls the game using three peripherals: the Razor Hydra, an occulus rift, and a mechanical set of paddles. The Hydra controls the arms and weapons of the Mech and the pedals are used for the movement of the legs.

{% include contributionItem.md proj=page %} 