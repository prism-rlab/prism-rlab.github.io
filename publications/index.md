---
title: Publications
description: Selected publications from PRISM Lab.
---

<section class="page-hero">
  <div class="container">
    <p class="eyebrow">Publications</p>
    <h1>Selected work from PRISM research areas.</h1>
    <p>This page starts with representative publication areas. Replace these entries with full citations as the lab publication list is finalized.</p>
  </div>
</section>

<section class="section">
  <div class="container publication-list">
    {% assign pubs = site.data.publications | sort: "year" | reverse %}
    {% for pub in pubs %}
      <article class="publication">
        <div class="pub-year">{{ pub.year }}</div>
        <div>
          <h2>{{ pub.title }}</h2>
          <p>{{ pub.authors }}</p>
          <p><strong>{{ pub.venue }}</strong> · {{ pub.area }}</p>
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
