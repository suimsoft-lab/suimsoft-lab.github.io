---
layout: splash
title: "모바일 앱 개발과 운영 기록"
author_profile: false
---

<section class="home-hero">
  <p class="page-chip">App · Web · Operations</p>
  <h1>앱과 웹 제품을 만들고 운영하는 개발 스튜디오입니다.</h1>
  <p>suimsoft-lab은 모바일 앱과 웹 서비스를 직접 기획, 개발, 배포하며 제품 소개와 기술 기록을 함께 정리합니다.</p>
  <div class="cta-wrap">
    <a class="btn btn--primary" href="/projects/">프로젝트 보기</a>
    <a class="btn btn--inverse" href="/devlog/">개발 로그 보기</a>
  </div>
</section>

<section class="content-section content-section--compact">
  <div class="workstream-grid">
    <a class="workstream-link" href="/projects/">
      <span>Product</span>
      <strong>프로젝트 홍보</strong>
      <em>앱 소개, 공개 링크, 운영 문서</em>
    </a>
    <a class="workstream-link" href="/devlog/">
      <span>Engineering</span>
      <strong>개발 기록</strong>
      <em>구현 과정, 설계 의도, 기술 선택</em>
    </a>
    <a class="workstream-link" href="/deployment/">
      <span>Operations</span>
      <strong>배포와 운영</strong>
      <em>릴리즈, 공지, 사후 대응 체크리스트</em>
    </a>
  </div>
</section>

<section class="content-section">
  <div class="section-heading">
    <p class="page-chip">Projects</p>
    <h2>프로젝트</h2>
    <p>현재 운영하거나 문서를 공개한 앱을 빠르게 확인할 수 있습니다.</p>
  </div>

  <div class="project-grid">
  {% for project in site.data.projects %}
    <article class="project-card project-card--{{ project.accent }}" id="{{ project.slug }}">
      <p class="project-card__meta">
        <span>{{ project.category }}</span>
        <span>{{ project.status }}</span>
      </p>
      <h3>{{ project.name }}</h3>
      <p>{{ project.summary }}</p>
      <p class="card-actions">
        <a class="btn btn--primary btn--small" href="{{ project.intro_url | relative_url }}">자세히 보기</a>
        <a class="btn btn--light-outline btn--small" href="{{ project.docs_url | relative_url }}">운영 문서</a>
        {% if project.play_url %}
          <a class="btn btn--light-outline btn--small" href="{{ project.play_url }}">Google Play</a>
        {% endif %}
      </p>
    </article>
  {% endfor %}
  </div>
</section>

<section class="content-section">
  <div class="section-heading">
    <p class="page-chip">Recent Notes</p>
    <h2>최신 글</h2>
    <p>프로젝트 소개, 개발 로그, 배포 운영 기록을 최신순으로 모았습니다.</p>
  </div>

{% assign latest_posts = site.posts | sort: "date" | reverse | slice: 0, 6 %}
<div class="latest-grid">
{% for post in latest_posts %}
  <article class="latest-card">
    <p class="latest-card__meta">
      <span class="category-badge">{{ post.categories | first }}</span>
      <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%Y-%m-%d" }}</time>
    </p>
    <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
    <p>{{ post.excerpt | strip_html | truncate: 110 }}</p>
  </article>
{% endfor %}
</div>
</section>

<section class="principle-strip">
  <div>
    <strong>정확성 우선</strong>
    <span>정책 정보는 참고용으로 제공하고 최종 확인 경로를 함께 안내합니다.</span>
  </div>
  <div>
    <strong>출처 명시</strong>
    <span>주요 정보는 공식 기관 출처 링크와 함께 정리합니다.</span>
  </div>
  <div>
    <strong>고지 준수</strong>
    <span>민간 서비스임을 명확히 안내해 사용자 혼동을 줄입니다.</span>
  </div>
</section>
