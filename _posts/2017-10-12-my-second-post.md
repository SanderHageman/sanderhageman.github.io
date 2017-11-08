---
layout: post
title: "My Second Post"
date: 2017-10-12
---


Second Post Test123
<br>
![My helpful screenshot]({{ "/assets/defaultThumb.jpg" | absolute_url }})
<br>

<div id="slider_container_2">
  <div id="SliderName_2">
    
    {% assign image_files = site.static_files | where: "image", true | where_exp: "myimage", "myimage.path contains 'my-pics1'"%}
    {% for myimage in image_files %}
    
    <img src="{{ myimage.path }}" width="700" height="450" alt="Demo2 second" title="Demo2 second" />
    <div class="SliderName_2Description">Featured model: <strong>Charlize Theron</strong></div>

    {% endfor %}
  </div>
  <div id="SliderNameNavigation_2"></div>
</div>

<script type="text/javascript">

  var demoSlider = Sliderman.slider({container: 'sName', width: 700, height: 450, effects: sEffects, display: sOptions});

</script>
