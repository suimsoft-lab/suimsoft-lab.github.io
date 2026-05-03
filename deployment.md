---
title: "Deployment"
permalink: /deployment/
layout: single
classes: content-index
---

<section class="section-hero">
  <p class="page-chip">Release & Operations</p>
  <h1>배포 후 운영과 사용자 안내</h1>
  <p>릴리즈 공지, 운영 체크리스트, 사후 대응 가이드를 실무 기준으로 정리합니다.</p>
</section>

{% assign items = site.posts | where_exp: "p", "p.categories contains 'deployment'" | sort: "date" | reverse %}
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
