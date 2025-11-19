---
title: "Equipe"
permalink: /equipe/
layout: single
---

Conheça os membros do nosso laboratório.

<div class="team-section">
  <h2>Professores</h2>
  <div class="team-grid">
    {% assign professores = site.equipe | where: "category", "Professores" %}
    {% for member in professores %}
    <div class="team-card">
      <div class="team-card-photo">
        <img src="{{ member.header.teaser }}" alt="{{ member.title }}">
      </div>
      <div class="team-card-info">
        <h3><a href="{{ member.lattes_url }}" target="_blank">{{ member.title }}</a></h3>
        <div class="position">{{ member.position }}</div>
        <div class="areas"><strong>Áreas:</strong> {{ member.areas }}</div>
      </div>
    </div>
    {% endfor %}
  </div>
</div>

<div class="team-section">
  <h2>Estudantes</h2>
  <div class="team-grid">
    {% assign estudantes = site.equipe | where: "category", "Estudantes" %}
    {% for member in estudantes %}
    <div class="team-card">
      <div class="team-card-photo">
        <img src="{{ member.header.teaser }}" alt="{{ member.title }}">
      </div>
      <div class="team-card-info">
        <h3><a href="{{ member.lattes_url }}" target="_blank">{{ member.title }}</a></h3>
        <div class="position">{{ member.position }}</div>
        <div class="areas"><strong>Áreas:</strong> {{ member.areas }}</div>
      </div>
    </div>
    {% endfor %}
  </div>
</div>
