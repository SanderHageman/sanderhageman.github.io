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

    {% endfor %}
  </div>
  <div id="SliderNameNavigation_2"></div>
</div>


<script type="text/javascript">
  effectsDemo2 = 'rain,stairs,fade';
  var demoSlider_2 = Sliderman.slider({container: 'SliderName_2', width: $( document ).width(), height: 450, effects: effectsDemo2,
    display: {
      autoplay: 3000,
      loading: {background: '#000000', opacity: 0.5, image: '{{ "/assets/sliderman/loading.gif" | absolute_url }}'},
      buttons: {hide: true, opacity: 1, prev: {className: 'SliderNamePrev_2', label: ''}, next: {className: 'SliderNameNext_2', label: ''}},
      navigation: {container: 'SliderNameNavigation_2', label: '<img src="{{ "/assets/sliderman/clear.gif" | absolute_url }}" />'}
    }
  });
</script>
