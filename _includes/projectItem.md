{% assign project = include.proj %}

{% assign thumbnail = site.static_files | where: "image", true | where: "thumbnail", true | where_exp: "myimage", "myimage.name contains project.title" %}

{% if thumbnail[0] == null %}
  {% assign thumbnail = site.static_files | where: "image", true | where: "thumbnail", true %}
{% endif %}

<div class="portfolioItem">
  <div class="thumb">
    <a href="{{ project.url }}">
      <img class="thumbnail" src="{{ thumbnail[0].path }}"/>
    </a>
  </div>
  <div class="desc">
    <p>
      <a href="{{ project.url }}">{{ project.title }}</a>
    </p>
    <p class="projDate">
      Date: {{ project.projectDate }}
    </p>
    <p class="projectSubtitle">
      {{ project.subtitle }}
    </p>
    <p>
      {% include contributionItemShortDesc.md proj = include.proj %}
    </p>
  </div>
</div>