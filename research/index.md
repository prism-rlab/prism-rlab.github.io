---
title: Research
description: Research themes at PRISM Lab.
---

<section class="page-hero">
  <div class="container">
    <p class="eyebrow">Research</p>
    <h1>Probabilistic intelligence for real-world systems.</h1>
    <p>PRISM works at the intersection of Bayesian inference, online learning, physics-guided machine learning, sensing, and intelligent decision-making.</p>
  </div>
</section>

<section class="section">
  <div class="container stack">
    {% for theme in site.data.research %}
      <article class="research-row">
        <div>
          <h2>{{ theme.title }}</h2>
          <p>{{ theme.summary }}</p>
        </div>
        <ul class="tag-list">
          {% for topic in theme.topics %}
            <li>{{ topic }}</li>
          {% endfor %}
        </ul>
      </article>
    {% endfor %}
  </div>
</section>
