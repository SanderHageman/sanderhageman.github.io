<ul>
  {% for item in include.proj.contributions %}
    <li>
      <strong>{{ item.name }}</strong>
      <ul>
        <li>
          {{ item.shortdesc }}
        </li>
      </ul>
    </li>
  {% endfor %}
</ul>