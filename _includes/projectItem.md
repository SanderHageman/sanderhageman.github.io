{% assign project = include.proj %}

{% assign thumbnail = site.static_files | where: "image", true | where: "thumbnail", true | where_exp: "myimage", "myimage.name contains project.title" %}

<div class="portfolioItem">
  <div class="thumb">
    <a href="{{ project.url }}">
      <img class="thumbnail" src="https://vnunen.nl/assets/portfolio/_thumbnails/einar.jpg?v=2"/>
    </a>
  
  {% comment %}
    <a class="thumbnail" href="{{ project.url }}" style="background-image: url('https://vnunen.nl/assets/portfolio/_thumbnails/einar.jpg?v=2');"></a>
    <a class="thumbnail" href="{{ project.url }}" style="background-image: url('{{ thumbnail[0].path }}');"></a>
  {% endcomment %}
  </div>
  <div class="desc">
    <p>
      <a href="{{ project.url }}">{{ project.title }}</a>
    </p>
    <p>
      {{ project.subtitle }}
    </p>
  </div>
</div>