---
title: Publications
description: Selected publications from PRISM Lab.
---

<section class="page-hero">
  <div class="container">
    <p class="eyebrow">Publications</p>
    <h1>Selected work from PRISM research areas.</h1>
    <p>A curated list of papers connected to the lab's core themes in probabilistic machine learning, recursive inference, physics-guided models, human-centered AI, remote sensing, and security.</p>
  </div>
</section>

<section class="section">
  <div class="container publication-groups">
    {% for group in site.data.publications.groups %}
      <section class="publication-topic">
        <div class="publication-topic-heading">
          <h2>{{ group.topic }}</h2>
          <p>{{ group.summary }}</p>
        </div>
        <div class="publication-list">
          {% for pub in group.papers %}
            <article class="publication">
              <div class="pub-year">{{ pub.year }}</div>
              <div>
                <h3>{{ pub.title }}</h3>
                <p class="pub-authors">{{ pub.authors }}</p>
                <p class="pub-meta"><strong>{{ pub.venue }}</strong></p>
                {% if pub.note %}<p class="publication-note">{{ pub.note }}</p>{% endif %}
                <div class="pub-links">
                  {% for link in pub.links %}
                    <a href="{{ link[1] }}">{{ link[0] | capitalize }}</a>
                  {% endfor %}
                </div>
              </div>
            </article>
          {% endfor %}
        </div>
      </section>
    {% endfor %}
  </div>
</section>
