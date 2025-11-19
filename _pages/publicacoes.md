---
title: "Publicações"
permalink: /publicacoes/
layout: single
---

Publicações científicas do laboratório.

<div class="publications-grid">
  {% assign publications = site.publicacoes | sort: 'date' | reverse %}
  {% for pub in publications %}
  <div class="publication-card">
    <h3><a href="{{ pub.pdf_url }}" target="_blank">{{ pub.title }}</a></h3>
    <div class="authors">{{ pub.authors }}</div>
    <div class="venue">{{ pub.venue }}</div>
  </div>
  {% endfor %}
</div>
