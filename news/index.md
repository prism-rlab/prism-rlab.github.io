---
title: News
description: News and updates from PRISM Lab.
---

<section class="page-hero">
  <div class="container">
    <p class="eyebrow">News</p>
    <h1>Updates from the lab.</h1>
    <p>Use this page for announcements, papers, grants, talks, student milestones, and recruiting updates.</p>
  </div>
</section>

<section class="section">
  <div class="container news-list wide">
    {% for item in site.data.news %}
      <article class="news-item">
        <time datetime="{{ item.date }}">{{ item.date | date: "%B %-d, %Y" }}</time>
        <h2>{{ item.title }}</h2>
        <p>{{ item.summary }}</p>
      </article>
    {% endfor %}
  </div>
</section>
