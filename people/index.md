---
title: People
description: People at PRISM Lab.
---

<section class="page-hero">
  <div class="container">
    <p class="eyebrow">People</p>
    <h1>The PRISM Lab community.</h1>
    <p>Add students, collaborators, visitors, and alumni here as the lab grows.</p>
  </div>
</section>

<section class="section">
  <div class="container people-grid">
    {% for person in site.data.people %}
      <article class="person-card">
        <img src="{{ person.image | relative_url }}" alt="">
        <div>
          <p class="person-role">{{ person.role }}</p>
          <h2>{{ person.name }}</h2>
          <p class="person-title">{{ person.title }}</p>
          <p>{{ person.bio }}</p>
          <div class="person-links">
            {% if person.website %}<a href="{{ person.website }}">Website</a>{% endif %}
            {% if person.github %}<a href="{{ person.github }}">GitHub</a>{% endif %}
          </div>
        </div>
      </article>
    {% endfor %}
  </div>
</section>
