---
title: "Projects"
permalink: /projects/
layout: single
classes: content-index
---

<section class="section-hero">
  <p class="page-chip">Project Showcase</p>
  <h1>운영 중인 제품과 공개 문서</h1>
  <p>앱의 문제 정의, 기능 구성, 운영 문서와 공개 링크를 프로젝트별로 정리합니다.</p>
</section>

<nav class="project-anchor-nav" aria-label="Project shortcuts">
{% for project in site.data.projects %}
  <a href="#{{ project.slug }}">{{ project.name }}</a>
{% endfor %}
</nav>

<div class="project-grid project-grid--wide">
{% for project in site.data.projects %}
  <article class="project-card project-card--{{ project.accent }}" id="{% if project.slug == 'hs-finder' %}hs-finder-card{% else %}{{ project.slug }}{% endif %}">
    <span class="project-card__mark" aria-hidden="true">{{ project.name | slice: 0 }}</span>
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

<section class="hs-showcase" id="hs-finder">
  <div class="hs-showcase__hero">
    <div class="hs-showcase__copy">
      <p class="page-chip">HS Finder</p>
      <h2>HS 코드 찾기 막막할 때, 제품 사진으로 후보를 확인하세요</h2>
      <p>
        수출입을 준비하다 보면 가장 먼저 마주치는 질문이 있습니다. 이 제품의 HS 코드는 무엇일까요?
        HS Finder는 제품 사진과 간단한 질문을 바탕으로 HS 코드 후보, 신뢰도, 분류 근거를 정리해 주는 AI 기반 품목분류 보조 앱입니다.
      </p>
      <div class="hs-showcase__actions">
        <a class="btn btn--primary" href="#hs-finder-how-to">사용 방법 보기</a>
        <a class="btn btn--light-outline" href="/hs-finder/privacy-policy/">개인정보처리방침</a>
      </div>
    </div>
    <div class="hs-showcase__visual" aria-label="HS Finder 앱 화면">
      <img src="{{ '/assets/images/hs-finder/home.jpg' | relative_url }}" alt="HS Finder 홈 화면">
    </div>
  </div>

  <div class="hs-showcase__notice">
    <strong>중요 안내</strong>
    <span>
      HS Finder의 결과는 참고용 권고 사항입니다. 최종 HS 코드 분류는 반드시 관세사, 세관, 무역 규정 전문가 등 자격 있는 전문가와 확인해야 합니다.
    </span>
  </div>

  <div class="hs-showcase__section">
    <div class="section-heading">
      <p class="page-chip">Who It Helps</p>
      <h2>이런 분께 추천합니다</h2>
      <p>품목분류 검색 전에 제품 정보를 정리하고, 전문가 상담에 필요한 기초 자료를 준비하려는 분께 적합합니다.</p>
    </div>
    <div class="hs-feature-grid">
      <article class="hs-feature">
        <h3>처음 수출입을 준비하는 사업자</h3>
        <p>제품명만으로 검색하기 어려울 때, 사진과 질문을 통해 검토할 정보를 먼저 정리할 수 있습니다.</p>
      </article>
      <article class="hs-feature">
        <h3>무역 실무 담당자</h3>
        <p>반복되는 품목 검토 전에 후보 코드와 확인 포인트를 빠르게 정리할 수 있습니다.</p>
      </article>
      <article class="hs-feature">
        <h3>온라인 셀러와 구매대행 운영자</h3>
        <p>상품 사진을 기반으로 대략적인 후보군을 파악하고 상담 자료를 준비할 수 있습니다.</p>
      </article>
      <article class="hs-feature">
        <h3>관세 상담 전 자료를 준비하는 분</h3>
        <p>소재, 용도, 원산지, 포장 등 핵심 정보를 한 흐름에서 점검할 수 있습니다.</p>
      </article>
    </div>
  </div>

  <div class="hs-showcase__section" id="hs-finder-how-to">
    <div class="section-heading">
      <p class="page-chip">How To Use</p>
      <h2>사용 방법은 간단합니다</h2>
    </div>
    <ol class="hs-steps">
      <li>
        <strong>제품 사진 촬영 또는 갤러리 이미지 선택</strong>
        제품 전체 모습, 라벨, 포장재, 제품 표시가 잘 보이는 밝은 사진을 사용하면 분석에 도움이 됩니다.
      </li>
      <li>
        <strong>AI 제품 분석 확인</strong>
        이미지에서 확인되는 제품 신호를 바탕으로 주요 추론 결과와 신뢰도를 보여줍니다.
      </li>
      <li>
        <strong>추가 질문에 답변</strong>
        제품명, 형태, 소재, 원산지, 포장, 세트 판매 여부처럼 HS 분류에 필요한 정보를 보완합니다.
      </li>
      <li>
        <strong>제품 프로필 검토</strong>
        입력한 답변이 요약되어 검색 전에 한 번 더 점검할 수 있습니다.
      </li>
      <li>
        <strong>HS 코드 후보 확인</strong>
        후보 코드, 매칭 점수, 분류 체계, 설명을 확인하고 전문가 검토용 자료로 활용합니다.
      </li>
    </ol>
  </div>

  <div class="hs-showcase__section">
    <div class="section-heading">
      <p class="page-chip">Screenshots</p>
      <h2>앱 화면 미리보기</h2>
      <p>사진 선택부터 분석, 질문, 제품 프로필, HS 코드 후보 확인까지 한 흐름으로 진행됩니다.</p>
    </div>
    <div class="hs-screenshot-grid">
      <figure>
        <img src="{{ '/assets/images/hs-finder/select-image.jpg' | relative_url }}" loading="lazy" alt="제품 이미지 선택 화면">
        <figcaption>제품 사진을 촬영하거나 갤러리에서 선택</figcaption>
      </figure>
      <figure>
        <img src="{{ '/assets/images/hs-finder/analysis.png' | relative_url }}" loading="lazy" alt="제품 분석 화면">
        <figcaption>AI 분석 결과와 신뢰도 확인</figcaption>
      </figure>
      <figure>
        <img src="{{ '/assets/images/hs-finder/question.png' | relative_url }}" loading="lazy" alt="제품 질문 입력 화면">
        <figcaption>HS 분류에 필요한 정보 보완</figcaption>
      </figure>
      <figure>
        <img src="{{ '/assets/images/hs-finder/profile.jpg' | relative_url }}" loading="lazy" alt="제품 프로필 화면">
        <figcaption>답변을 바탕으로 제품 프로필 검토</figcaption>
      </figure>
      <figure>
        <img src="{{ '/assets/images/hs-finder/result.jpg' | relative_url }}" loading="lazy" alt="HS 코드 결과 화면">
        <figcaption>후보 코드, 매칭 점수, 분류 체계 확인</figcaption>
      </figure>
    </div>
  </div>

  <div class="hs-showcase__section">
    <div class="section-heading">
      <p class="page-chip">Practical Use</p>
      <h2>실무에서는 이렇게 활용해 보세요</h2>
    </div>
    <p>
      해외 판매를 준비하는 상품이 있다면 먼저 HS Finder로 제품 사진을 등록해 보세요.
      앱에서 나온 후보 코드를 그대로 확정하기보다는, 제품 사양서, 소재 정보, 원산지, 용도, 판매 형태와 함께 검토 자료로 활용하는 것이 좋습니다.
    </p>
    <p>
      특히 처음 수출입을 준비하는 경우에는 HS 코드 자체보다도 내 제품을 어떤 기준으로 설명해야 하는지 파악하는 과정이 중요합니다.
      HS Finder는 제품 프로필과 질문 답변을 함께 정리해 이 과정을 쉽게 시작할 수 있도록 돕습니다.
    </p>
    <div class="hs-keywords">
      <strong>추천 검색 키워드</strong>
      <span>HS 코드, HS Code, 품목분류, 수출입, 통관, 관세, 무역 실무, 제품 분류, AI 무역 도구</span>
    </div>
  </div>
</section>

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
