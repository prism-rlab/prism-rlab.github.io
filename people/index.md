---
title: People
description: People at PRISM Lab.
---

<section class="page-hero">
  <div class="container">
    <p class="eyebrow">People</p>
    <h1>The PRISM Lab community.</h1>
    <p>PRISM brings together students working across probabilistic modeling, machine learning, intelligent systems, and computational science.</p>
  </div>
</section>

<section class="section">
  <div class="container people-section">
    <h2>Director</h2>
    <div class="people-grid featured">
      {% for person in site.data.people.director %}
      <article class="person-card">
        <img src="{{ person.image | relative_url }}" alt="">
        <div>
          <p class="person-role">{{ person.role }}</p>
          <h2>{{ person.name }}</h2>
          <p class="person-title">{{ person.title }}{% if person.program %}, {{ person.program }}{% endif %}</p>
          {% if person.status %}<p class="person-status">{{ person.status }}</p>{% endif %}
          {% if person.bio %}<p>{{ person.bio }}</p>{% endif %}
          <div class="person-links">
            {% if person.website %}<a href="{{ person.website }}">Website</a>{% endif %}
            {% if person.github %}<a href="{{ person.github }}">GitHub</a>{% endif %}
          </div>
        </div>
      </article>
      {% endfor %}
    </div>
  </div>
</section>

<section class="section section-muted">
  <div class="container people-section">
    <h2>PhD Students</h2>
    <div class="people-grid">
      {% for person in site.data.people.phd_students %}
        {% include person-card.html person=person %}
      {% endfor %}
    </div>
  </div>
</section>

<section class="section">
  <div class="container people-section">
    <h2>Master's Student</h2>
    <div class="people-grid compact">
      {% for person in site.data.people.masters_students %}
        {% include person-card.html person=person %}
      {% endfor %}
    </div>
  </div>
</section>

<section class="section section-muted">
  <div class="container people-section">
    <h2>Undergraduate Student</h2>
    <div class="people-grid compact">
      {% for person in site.data.people.undergraduate_students %}
        {% include person-card.html person=person %}
      {% endfor %}
    </div>
  </div>
</section>
