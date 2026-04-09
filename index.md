---
layout: splash
title: "모바일 앱 개발과 운영 기록"
author_profile: false
header:
  overlay_color: "#111827"
  actions:
    - label: "프로젝트 보기"
      url: "/projects/"
      class: "btn btn--primary"
    - label: "최신 개발 로그"
      url: "/devlog/"
      class: "btn btn--inverse"
---

`suimsoft-lab`은 육아/지원정책 도메인의 모바일 앱을 만들고 운영합니다.  
이 블로그에는 제품 소개, 기술 설계, 배포 운영 가이드를 함께 기록합니다.

## 앱 쇼케이스

<div class="app-grid">
  <article class="app-card">
    <h3>아기첫걸음</h3>
    <p>출산 후 필수 행정 절차와 지원금 신청 일정을 날짜 기준으로 안내하는 앱</p>
    <p class="app-card__actions">
      <a class="btn btn--primary btn--small" href="https://play.google.com/store/apps/details?id=com.babyfirststep.baby_first_step">Google Play</a>
      <a class="btn btn--light-outline btn--small" href="/projects/">소개 글</a>
    </p>
  </article>
  <article class="app-card">
    <h3>아이지원</h3>
    <p>임신·출산·육아 단계별 지원정책을 지역과 일정 기준으로 정리한 정책 가이드 앱</p>
    <p class="app-card__actions">
      <a class="btn btn--primary btn--small" href="https://play.google.com/store/apps/details?id=com.suimworks.babysupport">Google Play</a>
      <a class="btn btn--light-outline btn--small" href="/projects/">소개 글</a>
    </p>
  </article>
</div>

## 최신 글

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

## 운영 원칙

- **정확성 우선**: 정책 정보는 참고용으로 제공하고 최종 확인 경로를 함께 안내합니다.
- **출처 명시**: 주요 정보는 공식 기관 출처 링크를 함께 제공합니다.
- **고지 준수**: 민간 서비스임을 명확히 안내해 사용자 혼동을 줄입니다.

## 시작하기

<div class="cta-wrap">
  <a class="btn btn--primary" href="/projects/">프로젝트 전체 보기</a>
  <a class="btn btn--inverse" href="/devlog/">개발 기술 글 보기</a>
</div>
