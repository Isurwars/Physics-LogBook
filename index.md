---
layout: default         # Usa el layout principal (default.html)
title: Physics Logbook
---

# 🔭 Bitácora de Física Cuántica

¡Bienvenido(a) a mi bitácora de física! Este es un registro de mi viaje a través de la mecánica cuántica, la materia condensada y las simulaciones computacionales.

## Últimas Entradas

<ul class="post-list">
  {% for post in site.posts %}
    <li>
      <h3>
        <a class="post-link" href="{{ post.url | relative_url }}">{{ post.title | escape }}</a>
      </h3>
      <span class="post-meta">
        {{ post.date | date: "%Y-%m-%d" }}
        {% if post.categories %}
          | Categorías:
          {% for category in post.categories %}
            {{ category }}{% unless forloop.last %}, {% endunless %}
          {% endfor %}
        {% endif %}
      </span>
      <p>
        {{ post.excerpt | strip_html | strip_newlines | truncate: 150 }} 
        <a href="{{ post.url | relative_url }}">Leer más...</a>
      </p>
    </li>
  {% endfor %}
</ul>

<p class="rss-subscribe">Suscríbete vía <a href="{{ "/feed.xml" | relative_url }}">RSS</a></p>
