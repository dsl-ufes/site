---
title: "Equipe"
permalink: /equipe/
layout: archive
---
<!-- Removendo o título colocado automaticamente pelo Jekyll -->
<style>
  .page__title { display: none !important; }
</style>

<h1 style="text-transform: uppercase; font-size: 1.6em; letter-spacing: 2px; color: #000; margin-top: 0; margin-bottom: 1em; border-bottom: 2px solid #000; padding-bottom: 10px;">Equipe</h1>

<p style="margin-bottom: 3.5em; color: #333; font-size: 1.05em;">Conheça os membros do nosso laboratório.</p>

<div style="margin-bottom: 5em;">
  <h2 style="text-transform: uppercase; font-size: 1.2em; letter-spacing: 1px; color: #000; margin-bottom: 2em; border-bottom: 1px solid #000; padding-bottom: 8px;">Professores</h2>

  <div style="display: grid; grid-template-columns: repeat(auto-fill, minmax(220px, 1fr)); gap: 40px 30px;">
    {% assign professores = site.equipe | where: "category", "Professores" %}
    {% for member in professores %}
    <div style="display: flex; flex-direction: column;">
      <div style="margin-bottom: 1.2em;">
        <img src="{{ member.header.teaser | relative_url }}" alt="{{ member.title }}" style="width: 100%; aspect-ratio: 1/1; object-fit: cover; border: 1px solid #000; display: block;">
      </div>
      <h3 style="margin: 0 0 0.3em 0; font-size: 1.15em; line-height: 1.3;">
        <a href="{{ member.lattes_url }}" target="_blank" style="text-decoration: none; color: #000;">{{ member.title }}</a>
      </h3>
      <div style="font-size: 0.75em; text-transform: uppercase; letter-spacing: 1px; color: #555; margin-bottom: 1em;">
        {{ member.position }}
      </div>
      <div style="font-size: 0.9em; color: #333; line-height: 1.5; margin-bottom: 1.5em; flex-grow: 1;">
        <strong style="color: #000;">Áreas:</strong> {{ member.areas }}
      </div>

      {% if member.email %}
      <div style="margin-top: auto;">
        <a href="mailto:{{ member.email }}" style="display: inline-block; padding: 0.5em 1.2em; border: 1px solid #000; color: #000; text-decoration: none; font-weight: bold; text-transform: uppercase; font-size: 0.75em; letter-spacing: 0.5px; transition: background-color 0.2s ease, color 0.2s ease;" onmouseover="this.style.backgroundColor='#000'; this.style.color='#fff';" onmouseout="this.style.backgroundColor='transparent'; this.style.color='#000';">Contato</a>
      </div>
      {% endif %}
    </div>
    {% endfor %}
  </div>
</div>

<div style="margin-bottom: 3em;">
  <h2 style="text-transform: uppercase; font-size: 1.2em; letter-spacing: 1px; color: #000; margin-bottom: 2em; border-bottom: 1px solid #000; padding-bottom: 8px;">Estudantes</h2>

  <div style="display: grid; grid-template-columns: repeat(auto-fill, minmax(220px, 1fr)); gap: 40px 30px;">
    {% assign estudantes = site.equipe | where: "category", "Estudantes" %}
    {% for member in estudantes %}
    <div style="display: flex; flex-direction: column;">
      <div style="margin-bottom: 1.2em;">
        <img src="{{ member.header.teaser | relative_url }}" alt="{{ member.title }}" style="width: 100%; aspect-ratio: 1/1; object-fit: cover; border: 1px solid #000; display: block;">
      </div>
      <h3 style="margin: 0 0 0.3em 0; font-size: 1.15em; line-height: 1.3;">
        <a href="{{ member.lattes_url }}" target="_blank" style="text-decoration: none; color: #000;">{{ member.title }}</a>
      </h3>
      <div style="font-size: 0.75em; text-transform: uppercase; letter-spacing: 1px; color: #555; margin-bottom: 1em;">
        {{ member.position }}
      </div>
      <div style="font-size: 0.9em; color: #333; line-height: 1.5; margin-bottom: 1.5em; flex-grow: 1;">
        <strong style="color: #000;">Áreas:</strong> {{ member.areas }}
      </div>

      {% if member.email %}
      <div style="margin-top: auto;">
        <a href="mailto:{{ member.email }}" style="display: inline-block; padding: 0.5em 1.2em; border: 1px solid #000; color: #000; text-decoration: none; font-weight: bold; text-transform: uppercase; font-size: 0.75em; letter-spacing: 0.5px; transition: background-color 0.2s ease, color 0.2s ease;" onmouseover="this.style.backgroundColor='#000'; this.style.color='#fff';" onmouseout="this.style.backgroundColor='transparent'; this.style.color='#000';">Contato</a>
      </div>
      {% endif %}
    </div>
    {% endfor %}
  </div>
</div>