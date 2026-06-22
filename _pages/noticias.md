---
title: "Notícias"
permalink: /noticias/
layout: archive
---

<h1 style="text-transform: uppercase; font-size: 1.6em; letter-spacing: 2px; color: #000; margin-top: 0; margin-bottom: 2em; border-bottom: 2px solid #000; padding-bottom: 10px;">Notícias</h1>

<div class="news-archive-main">
  {% if paginator %}
    {% assign news_posts = paginator.posts %}
  {% else %}
    {% assign news_posts = site.posts %}
  {% endif %}

  {% for post in news_posts %}
    <div class="news-item" style="margin-bottom: 3.5em; padding-bottom: 2.5em; border-bottom: 1px solid #000; display: flex; gap: 30px; flex-wrap: wrap; align-items: flex-start;">
      
      {% if post.header.teaser %}
      <div style="flex: 1 1 200px; max-width: 240px;">
        <img src="{{ post.header.teaser | relative_url }}" alt="{{ post.title }}" style="width: 100%; object-fit: cover; border: 1px solid #000; filter: grayscale(100%);">
      </div>
      {% endif %}
      
      <div style="flex: 2 1 300px; display: flex; flex-direction: column;">
        <span style="font-size: 0.8em; text-transform: uppercase; letter-spacing: 1px; color: #555; margin-bottom: 0.5em;">
          {{ post.date | date: "%d/%m/%Y" }}
        </span>
        <h2 style="margin: 0 0 0.6em 0; font-size: 1.4em; line-height: 1.3; font-weight: bold;">
          <a href="{{ post.url | relative_url }}" style="text-decoration: none; color: #000;">{{ post.title }}</a>
        </h2>
        <p style="margin: 0 0 1.8em 0; color: #333; line-height: 1.6; font-size: 0.95em;">
          {{ post.excerpt | strip_html | truncatewords: 35 }}
        </p>
        <div>
          <a href="{{ post.url | relative_url }}" style="display: inline-block; padding: 0.5em 1.2em; border: 1px solid #000; color: #000; background-color: transparent; text-decoration: none; font-weight: bold; text-transform: uppercase; font-size: 0.75em; letter-spacing: 0.5px;">Ler Notícia</a>
        </div>
      </div>
      
    </div>
  {% else %}
    <p style="color: #000;">Nenhuma notícia publicada de momento.</p>
  {% endfor %}
</div>

{% include paginator.html %}