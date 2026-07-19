---
layout: default
title: Fotografia
navigation: true
nav_order: 4
---

# Galleria Eventi

In questa sezione raccolgo le foto realizzate per diversi eventi e viaggi. Clicca per visualizzare la descrizione, i dettagli e accedere alla galleria fotografica.

<ul class="event-list" style="list-style: none; padding-left: 0;">
  {% assign sorted_events = site.fotografia | reverse %}
  {% for event in sorted_events %}
    <li style="margin-bottom: 2rem; padding: 1.5rem; background: var(--1); border-radius: 20px;">
      <h3 style="margin-bottom: 0.5rem;"><a href="{{ event.url | relative_url }}">{{ event.title }}</a></h3>
      <p style="color: #666; font-size: 0.9rem; margin-top: 0; margin-bottom: 0.8rem;">
        {% if event.date_formatted %}
          <span style="margin-right: 15px;">{{ event.date_formatted }}</span>
        {% endif %}
        {% if event.location %}
          <span>{{ event.location }}</span>
        {% endif %}
      </p>
      {% if event.description %}
        <p>{{ event.description }}</p>
      {% endif %}
    </li>
  {% endfor %}
</ul>
