---
title: "Devlog"
permalink: /devlog/
layout: single
---

<section class="section-hero">
  <p class="page-chip">Developer Notes</p>
  <h2>설계 의도와 구현 디테일</h2>
  <p>기능 구현 과정, 아키텍처 선택, 트러블슈팅과 성능/운영 관점의 기술 기록을 남깁니다.</p>
</section>

{% assign items = site.posts | where_exp: "p", "p.categories contains 'devlog'" | sort: "date" | reverse %}
<div class="post-grid">
{% for post in items %}
  <article class="post-card">
    <p class="latest-card__meta">
      <span class="category-badge">{{ post.categories | first }}</span>
      <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%Y-%m-%d" }}</time>
    </p>
    <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
    <p>{{ post.excerpt | strip_html | truncate: 120 }}</p>
  </article>
{% endfor %}
</div>
