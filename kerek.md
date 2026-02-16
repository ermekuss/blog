---
layout: default
title: Kerek
permalink: /kerek/
---

<section class="page">
  <div class="container">
    <h1>Kerek</h1>
    <p>Полезные ссылки для учёных. Добавляйте сюда сервисы, базы данных, гранты и инструменты.</p>

    <div class="item">
      <ul>
        <li><a href="https://scholar.google.com/">Google Scholar</a> — поиск научных публикаций.</li>
        <li><a href="https://orcid.org/">ORCID</a> — идентификатор исследователя.</li>
        <li><a href="https://www.zotero.org/">Zotero</a> — менеджер библиографии.</li>
      </ul>
      <p class="small">Замените/дополните список своими ссылками.</p>
    </div>

    <h2 style="margin-top:22px;">Посты в разделе</h2>
    <div class="list">
      {% assign items = site.posts | where_exp: "p", "p.categories contains 'kerek'" %}
      {% for post in items %}
        <div class="item">
          <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
          <div class="small">{{ post.date | date: "%d.%m.%Y" }}</div>
          <div class="small">{{ post.excerpt | strip_html | truncate: 180 }}</div>
        </div>
      {% endfor %}
      {% if items.size == 0 %}
        <div class="item">Пока нет постов в разделе Kerek.</div>
      {% endif %}
    </div>
  </div>
</section>
