---
layout: default
title: Maqala
permalink: /maqala/
---

<section class="page">
  <div class="container">
    <h1>Maqala</h1>
    <p>Краткие обзоры моих статей, работ коллег и интересных публикаций, которые я прочитал.</p>

    <div class="list">
      {% assign items = site.posts | where_exp: "p", "p.categories contains 'maqala'" %}
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
