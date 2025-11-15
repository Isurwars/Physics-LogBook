---
layout: default         # Usa el layout principal (default.html)
title: Physics Logbook
---

# ⚛️ Quantum Physics Logbook

Welcome to my physics logbook! This is a record of my journey through quantum mechanics, condensed matter, and computational simulations.

🙋 About the Logbook

This space serves as my digital laboratory notebook and learning journal. Here I document:

- Experiments and Simulations: Details of the setup and results of my practical work.

- Theoretical Concepts: Detailed explanations of topics like the electronic structure of graphene or the Bloch formalism.

- Code Development: Snippets of Python, Julia, or C++ for calculations and visualizations.

My goal is to consolidate knowledge and share ideas with the community.

# 📂 Latest Entries

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
