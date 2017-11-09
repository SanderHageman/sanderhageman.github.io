---
layout: post
title: "My Second Post"
date: 2017-10-12
---


Second Post Test123
<br>
![My helpful screenshot]({{ "/assets/defaultThumb.jpg" | absolute_url }})
<br>

<div class="slider-wrapper theme-default">
<div id="slider" class="nivoSlider">     
    {% assign image_files = site.static_files | where: "image", true | where_exp: "myimage", "myimage.path contains 'my-pics1'"%}
    {% for myimage in image_files %}
    
    <img src="{{ myimage.path }}"/>

    {% endfor %}
</div> <!-- nivoSlider -->
</div> <!-- slider-wrapper theme -->

<div id="htmlcaption" class="nivo-html-caption">     
    <strong>This</strong> is an example of a <em>HTML</em> caption with <a href="#">a link</a>. 
</div>

<script type="text/javascript"> 
$(window).on('load', function() {
    var metaslider_363 = function($) {
        $('#metaslider_363').nivoSlider({ 
            boxCols:7,
            boxRows:5,
            pauseTime:3000,
            effect:"fade",
            controlNav:true,
            directionNav:true,
            pauseOnHover:true,
            animSpeed:600,
            prevText:"&lt;",
            nextText:"&gt;",
            slices:15,
            manualAdvance:false
        });
    };
    
    
    
    $('#slider').nivoSlider(); 
}); 
</script>
