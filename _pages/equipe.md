---
title: "Equipe"
permalink: /equipe/
layout: archive
---
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
      <div style="margin-top: auto; padding-top: 0.5em;">
        <a href="mailto:{{ member.email }}" style="display: flex; align-items: center; color: #000; text-decoration: none; font-size: 0.85em; word-break: break-all; transition: opacity 0.2s ease;" onmouseover="this.style.textDecoration='underline';" onmouseout="this.style.textDecoration='none';">
          <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round" style="margin-right: 8px; flex-shrink: 0;"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"></path><polyline points="22,6 12,13 2,6"></polyline></svg>
          {{ member.email }}
        </a>
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
      <div style="margin-top: auto; padding-top: 0.5em;">
        <a href="mailto:{{ member.email }}" style="display: flex; align-items: center; color: #000; text-decoration: none; font-size: 0.85em; word-break: break-all; transition: opacity 0.2s ease;" onmouseover="this.style.textDecoration='underline';" onmouseout="this.style.textDecoration='none';">
          <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round" style="margin-right: 8px; flex-shrink: 0;"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"></path><polyline points="22,6 12,13 2,6"></polyline></svg>
          {{ member.email }}
        </a>
      </div>
      {% endif %}
    </div>
    {% endfor %}
  </div>
</div>