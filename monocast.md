---
layout: default
title: Monocast
permalink: /monocast/
---

<section class="page">
  <div class="container">
    <h1>Monocast</h1>
    <p>Выпуски моего подкаста. Здесь удобно размещать плееры и ссылки на платформы.</p>

    <div class="list">
      {% assign items = site.posts | where_exp: "p", "p.categories contains 'monocast'" %}
      {% for post in items %}
        <div class="item">
          <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
          <div class="small">{{ post.date | date: "%d.%m.%Y" }}</div>
          <div class="small">{{ post.excerpt | strip_html | truncate: 180 }}</div>
        </div>
      {% endfor %}
      {% if items.size == 0 %}
        <div class="item">Пока нет материалов в этом разделе.</div>
      {% endif %}
    </div>
  </div>
</section>
