---
title: "Projects"
permalink: /projects/
layout: single
---

<section class="section-hero">
  <p class="page-chip">Project Showcase</p>
  <h2>모바일 앱 소개와 업데이트</h2>
  <p>앱의 문제 정의, 기능 구성, 사용자 가치, 운영 방향을 제품 중심으로 정리합니다.</p>
</section>

{% assign items = site.posts | where_exp: "p", "p.categories contains 'project'" | sort: "date" | reverse %}
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
