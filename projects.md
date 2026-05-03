---
title: "Projects"
permalink: /projects/
layout: single
classes: content-index
---

<section class="section-hero">
  <p class="page-chip">Project Showcase</p>
  <h1>프로젝트</h1>
  <p>앱의 문제 정의, 기능 구성, 운영 문서와 공개 링크를 프로젝트별로 정리합니다.</p>
</section>

<nav class="project-anchor-nav" aria-label="Project shortcuts">
{% for project in site.data.projects %}
  <a href="#{{ project.slug }}">{{ project.name }}</a>
{% endfor %}
</nav>

<div class="project-grid project-grid--wide">
{% for project in site.data.projects %}
  <article class="project-card project-card--{{ project.accent }}" id="{{ project.slug }}">
    <p class="project-card__meta">
      <span>{{ project.category }}</span>
      <span>{{ project.status }}</span>
    </p>
    <h2>{{ project.name }}</h2>
    <p>{{ project.summary }}</p>
    <p class="card-actions">
      <a class="btn btn--primary btn--small" href="{{ project.intro_url | relative_url }}">소개 보기</a>
      <a class="btn btn--light-outline btn--small" href="{{ project.docs_url | relative_url }}">운영 문서</a>
      {% if project.play_url %}
        <a class="btn btn--light-outline btn--small" href="{{ project.play_url }}">Google Play</a>
      {% endif %}
    </p>
  </article>
{% endfor %}
</div>

<section class="content-section">
  <div class="section-heading">
    <p class="page-chip">Project Notes</p>
    <h2>프로젝트 소개 글</h2>
  </div>

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
</section>
