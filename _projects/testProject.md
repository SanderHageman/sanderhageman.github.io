---
layout: post
title: "testProject"
subtitle: "Testing different folder struct"
---

Second Post Test123
<!-- [My helpful screenshot]({{ "/assets/defaultThumb.jpg" | absolute_url }}) -->

<div class="slider-wrapper theme-bar">
<div id="slider" class="nivoSlider">     
    {% assign image_files = site.static_files | where: "image", true | where_exp: "myimage", "myimage.path contains 'my-pics1'"%}
    {% for myimage in image_files %}
    
    <img src="{{ myimage.path }}"/>

    {% endfor %}
</div> <!-- nivoSlider -->
</div> <!-- slider-wrapper theme -->

<script type="text/javascript"> 
$(window).on('load', function() {
    $('#slider').nivoSlider({
        effect: 'fade',
        animSpeed: 600
    });
}); 
</script>
