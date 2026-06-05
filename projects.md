---
title: "운영 중인 앱 프로젝트"
permalink: /projects/
layout: single
classes: content-index
description: "suimsoft-lab이 운영 중인 아기첫걸음, 아이지원, HS Finder 앱의 핵심 기능, Google Play 링크, 개인정보처리방침과 운영 문서를 모아 둔 프로젝트 소개 페이지입니다."
excerpt: "아기첫걸음, 아이지원, HS Finder 앱의 기능, Google Play 링크, 운영 문서를 한곳에서 확인하세요."
header:
  og_image: /assets/images/baby-first-step/home.png
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
  <article class="project-card project-card--{{ project.accent }}" id="{% if project.slug == 'baby-first-step' or project.slug == 'ijiwon' or project.slug == 'hs-finder' %}{{ project.slug }}-card{% else %}{{ project.slug }}{% endif %}">
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

<section class="hs-showcase" id="baby-first-step">
  <div class="hs-showcase__hero">
    <div class="hs-showcase__copy">
      <p class="page-chip">Baby First Step</p>
      <h2>출산 직후 해야 할 행정 절차와 지원금을 날짜 기준으로 정리하세요</h2>
      <p>
        아기첫걸음은 출생일을 기준으로 출생신고, 건강보험 등록, 부모급여 신청처럼 놓치기 쉬운 초기 행정 절차를
        D-day 타임라인으로 보여주는 육아 행정 안내 앱입니다. 중앙정부와 서울시 지원금 정보를 함께 정리해
        출산 직후 가족이 지금 해야 할 일을 빠르게 확인할 수 있도록 돕습니다.
      </p>
      <div class="hs-showcase__actions">
        <a class="btn btn--primary" href="/project/baby-first-step-intro/">소개 글 보기</a>
        <a class="btn btn--light-outline" href="https://play.google.com/store/apps/details?id=com.babyfirststep.baby_first_step">Google Play</a>
        <a class="btn btn--light-outline" href="/baby-first-step/privacy/">개인정보처리방침</a>
      </div>
      <p>
        Android 앱으로 제공되며, 가족 코드와 Google 로그인을 통해 배우자나 가족과 체크 상태를 함께 관리할 수 있습니다.
      </p>
    </div>
    <div class="hs-showcase__visual" aria-label="아기첫걸음 앱 화면">
      <img src="{{ '/assets/images/baby-first-step/home.png' | relative_url }}" alt="아기첫걸음 홈 화면">
    </div>
  </div>

  <div class="hs-showcase__notice">
    <strong>중요 안내</strong>
    <span>
      아기첫걸음의 행정 절차와 지원금 정보는 참고용입니다. 신청 전 실제 대상 조건, 금액, 접수 기간은 정부24, 복지로, 관할 주민센터 등 공식 기관에서 최종 확인해야 합니다.
    </span>
  </div>

  <div class="hs-showcase__section">
    <div class="section-heading">
      <p class="page-chip">Who It Helps</p>
      <h2>이런 가족에게 적합합니다</h2>
      <p>출산 직후 행정 처리와 지원금 신청을 한 번에 정리하고 싶은 부모와 가족을 위한 앱입니다.</p>
    </div>
    <div class="hs-feature-grid">
      <article class="hs-feature">
        <h3>출산 직후 무엇부터 할지 막막한 부모</h3>
        <p>출생일 기준으로 지금 처리해야 할 일과 앞으로 다가올 절차를 순서대로 확인할 수 있습니다.</p>
      </article>
      <article class="hs-feature">
        <h3>지원금 신청을 놓치고 싶지 않은 가족</h3>
        <p>첫만남이용권, 부모급여, 아동수당 등 주요 지원 제도를 한 화면에서 살펴볼 수 있습니다.</p>
      </article>
      <article class="hs-feature">
        <h3>부부가 함께 체크리스트를 관리하는 가정</h3>
        <p>6자리 가족 코드로 진행 상태를 공유해 누가 어떤 절차를 완료했는지 쉽게 맞출 수 있습니다.</p>
      </article>
      <article class="hs-feature">
        <h3>서울시 출산 지원 정보를 찾는 사용자</h3>
        <p>중앙정부 지원뿐 아니라 서울시 산후조리경비, 임산부 교통비 같은 지역 정보를 함께 확인합니다.</p>
      </article>
    </div>
  </div>

  <div class="hs-showcase__section">
    <div class="section-heading">
      <p class="page-chip">How To Use</p>
      <h2>출생일만 입력하면 일정이 정리됩니다</h2>
    </div>
    <ol class="hs-steps">
      <li>
        <strong>아기 정보와 출생일 입력</strong>
        출생일을 기준으로 D+7, D+14, D+30, D+60, D+100 등 주요 시점을 자동으로 계산합니다.
      </li>
      <li>
        <strong>행정 절차 체크</strong>
        출생신고, 건강보험 등록, 양육수당 및 부모급여 신청 등 9개 절차의 상태를 완료로 표시할 수 있습니다.
      </li>
      <li>
        <strong>지원금 정보 확인</strong>
        중앙정부와 서울시 지원 항목을 확인하고, 필요한 경우 공식 신청 경로로 이동합니다.
      </li>
      <li>
        <strong>가족과 동기화</strong>
        가족 코드를 공유해 배우자나 가족의 기기에서도 같은 체크리스트와 설정을 확인합니다.
      </li>
      <li>
        <strong>알림으로 기한 관리</strong>
        중요한 절차의 시작일과 마감 전날 알림을 받아 바쁜 초기 육아 시기에 누락을 줄입니다.
      </li>
    </ol>
  </div>

  <div class="hs-showcase__section">
    <div class="section-heading">
      <p class="page-chip">Screenshots</p>
      <h2>앱 화면 미리보기</h2>
      <p>오늘 할 일, 행정 절차, 지원금, 가족 동기화 설정까지 출산 직후 필요한 흐름을 중심으로 구성했습니다.</p>
    </div>
    <div class="hs-screenshot-grid">
      <figure>
        <img src="{{ '/assets/images/baby-first-step/home.png' | relative_url }}" loading="lazy" alt="아기첫걸음 홈 화면">
        <figcaption>D-day 타임라인과 오늘 확인할 일</figcaption>
      </figure>
      <figure>
        <img src="{{ '/assets/images/baby-first-step/procedures.png' | relative_url }}" loading="lazy" alt="아기첫걸음 행정 절차 화면">
        <figcaption>출산 후 행정 절차 체크리스트</figcaption>
      </figure>
      <figure>
        <img src="{{ '/assets/images/baby-first-step/subsidies.png' | relative_url }}" loading="lazy" alt="아기첫걸음 지원금 화면">
        <figcaption>중앙정부와 서울시 지원금 안내</figcaption>
      </figure>
      <figure>
        <img src="{{ '/assets/images/baby-first-step/settings.png' | relative_url }}" loading="lazy" alt="아기첫걸음 설정 화면">
        <figcaption>아기 정보, 지역, 가족 동기화 설정</figcaption>
      </figure>
    </div>
  </div>

  <div class="hs-showcase__section">
    <div class="section-heading">
      <p class="page-chip">Practical Use</p>
      <h2>출산 준비 체크리스트가 아니라 출산 직후 실행표입니다</h2>
    </div>
    <p>
      출산 전에는 준비물 체크리스트가 필요하지만, 출산 직후에는 기한이 있는 행정 절차와 신청 일정이 더 중요해집니다.
      아기첫걸음은 가족이 흩어진 정보를 다시 찾지 않아도 되도록, 날짜 기준으로 해야 할 일을 정리하고 완료 상태를 남길 수 있게 설계했습니다.
    </p>
    <p>
      특히 첫 아이를 맞이한 가정에서는 어떤 지원을 받을 수 있는지보다 먼저 어떤 순서로 확인해야 하는지가 어렵습니다.
      앱은 핵심 절차와 대표 지원 제도를 먼저 보여주고, 세부 조건은 공식 기관에서 확인하도록 안내합니다.
    </p>
    <div class="hs-keywords">
      <strong>추천 검색 키워드</strong>
      <span>출생신고, 부모급여, 첫만남이용권, 아동수당, 출산 지원금, 산후조리경비, 신생아 행정 절차, 육아 체크리스트</span>
    </div>
  </div>
</section>

<section class="hs-showcase" id="ijiwon">
  <div class="hs-showcase__hero">
    <div class="hs-showcase__copy">
      <p class="page-chip">아이지원</p>
      <h2>임신부터 육아까지 받을 수 있는 공공 지원정책을 한눈에 확인하세요</h2>
      <p>
        아이지원은 임신, 출산, 육아 단계별 공공 지원정책을 지역과 생애주기 기준으로 정리하는 정책 가이드 앱입니다.
        45개 지원정책을 카테고리, 지역, 키워드로 필터링하고, 신청 대상과 혜택, 신청 방법, 공식 사이트를 함께 확인할 수 있습니다.
      </p>
      <div class="hs-showcase__actions">
        <a class="btn btn--primary" href="/project/baby-support-intro/">소개 글 보기</a>
        <a class="btn btn--light-outline" href="https://play.google.com/store/apps/details?id=com.suimworks.babysupport">Google Play</a>
        <a class="btn btn--light-outline" href="/ijiwon/privacy/">개인정보처리방침</a>
      </div>
      <p>
        Android 앱으로 제공되며, D-day와 지역 설정을 바탕으로 사용자 상황에 맞는 정책과 타임라인을 보여줍니다.
      </p>
    </div>
    <div class="hs-showcase__visual" aria-label="아이지원 앱 화면">
      <img src="{{ '/assets/images/ijiwon/home.png' | relative_url }}" alt="아이지원 홈 화면">
    </div>
  </div>

  <div class="hs-showcase__notice">
    <strong>중요 안내</strong>
    <span>
      아이지원의 정책 정보는 참고용입니다. 지원 금액, 대상 조건, 신청 기간은 변경될 수 있으므로 신청 전 각 기관 공식 홈페이지에서 직접 확인해야 합니다.
    </span>
  </div>

  <div class="hs-showcase__section">
    <div class="section-heading">
      <p class="page-chip">Who It Helps</p>
      <h2>이런 분께 추천합니다</h2>
      <p>정책 이름보다 내 상황에서 지금 확인해야 할 지원을 먼저 알고 싶은 예비부모와 양육 가정을 위한 앱입니다.</p>
    </div>
    <div class="hs-feature-grid">
      <article class="hs-feature">
        <h3>임신 중 받을 수 있는 지원을 찾는 예비부모</h3>
        <p>임신 단계에서 확인해야 할 전국, 서울시, 자치구 정책을 빠르게 좁혀 볼 수 있습니다.</p>
      </article>
      <article class="hs-feature">
        <h3>출산 지원금과 서비스가 헷갈리는 가족</h3>
        <p>지원 대상, 혜택, 신청 방법을 정책별로 나눠 보고 공식 신청 사이트로 이동할 수 있습니다.</p>
      </article>
      <article class="hs-feature">
        <h3>육아 단계별 일정을 관리하려는 사용자</h3>
        <p>D-day 기반 타임라인으로 임신, 출산, 육아 과정에서 놓치기 쉬운 확인 항목을 정리합니다.</p>
      </article>
      <article class="hs-feature">
        <h3>지역별 지원 정보를 비교하는 사용자</h3>
        <p>지역 필터와 키워드 검색으로 내 거주 지역과 관련 있는 정책을 먼저 확인할 수 있습니다.</p>
      </article>
    </div>
  </div>

  <div class="hs-showcase__section">
    <div class="section-heading">
      <p class="page-chip">How To Use</p>
      <h2>정책 탐색부터 신청 경로 확인까지 이어집니다</h2>
    </div>
    <ol class="hs-steps">
      <li>
        <strong>D-day와 지역 설정</strong>
        임신, 출산, 육아 상황과 거주 지역을 입력해 사용자에게 맞는 정책 탐색 기준을 만듭니다.
      </li>
      <li>
        <strong>추천 정책 확인</strong>
        홈에서 현재 시점에 가까운 추천 정책과 마감 임박 정보를 먼저 확인합니다.
      </li>
      <li>
        <strong>카테고리와 키워드로 필터링</strong>
        결혼, 임신, 출산, 육아 카테고리와 지역, 검색어로 필요한 정책만 좁혀 봅니다.
      </li>
      <li>
        <strong>정책 상세 검토</strong>
        지원 대상, 혜택, 신청 기간, 신청 방법, 유의사항을 상세 화면에서 확인합니다.
      </li>
      <li>
        <strong>공식 사이트에서 최종 확인</strong>
        앱의 바로가기 링크를 통해 공식 기관 페이지로 이동해 최신 공고와 신청 조건을 확인합니다.
      </li>
    </ol>
  </div>

  <div class="hs-showcase__section">
    <div class="section-heading">
      <p class="page-chip">Screenshots</p>
      <h2>앱 화면 미리보기</h2>
      <p>추천 정책, 정책 목록, 상세 정보, 타임라인, 설정까지 정책 확인에 필요한 주요 화면을 담았습니다.</p>
    </div>
    <div class="hs-screenshot-grid">
      <figure>
        <img src="{{ '/assets/images/ijiwon/home.png' | relative_url }}" loading="lazy" alt="아이지원 홈 화면">
        <figcaption>D-day 요약과 추천 정책</figcaption>
      </figure>
      <figure>
        <img src="{{ '/assets/images/ijiwon/policy-list.png' | relative_url }}" loading="lazy" alt="아이지원 정책 목록 화면">
        <figcaption>카테고리, 지역, 키워드 기반 정책 목록</figcaption>
      </figure>
      <figure>
        <img src="{{ '/assets/images/ijiwon/policy-detail.png' | relative_url }}" loading="lazy" alt="아이지원 정책 상세 화면">
        <figcaption>지원 대상, 혜택, 신청 방법 상세 확인</figcaption>
      </figure>
      <figure>
        <img src="{{ '/assets/images/ijiwon/timeline.png' | relative_url }}" loading="lazy" alt="아이지원 타임라인 화면">
        <figcaption>생애주기별 맞춤 체크리스트</figcaption>
      </figure>
      <figure>
        <img src="{{ '/assets/images/ijiwon/settings.png' | relative_url }}" loading="lazy" alt="아이지원 설정 화면">
        <figcaption>D-day, 지역, 알림, 법적 고지 설정</figcaption>
      </figure>
    </div>
  </div>

  <div class="hs-showcase__section">
    <div class="section-heading">
      <p class="page-chip">Practical Use</p>
      <h2>정책 검색 시간을 줄이고 공식 확인으로 이어지게 합니다</h2>
    </div>
    <p>
      임신과 출산, 육아 지원정책은 기관과 지역에 따라 이름과 조건이 다르고 자주 바뀝니다.
      아이지원은 정책을 단계와 지역 기준으로 먼저 정리해 사용자가 자신에게 관련 있는 제도를 빠르게 찾도록 돕습니다.
    </p>
    <p>
      앱에서 정책 개요를 확인한 뒤에는 상세 화면의 공식 사이트 링크로 이동해 최신 공고와 신청 조건을 다시 확인하는 흐름을 권장합니다.
      정책 정보를 단순히 모아 두는 데서 끝나지 않고 실제 신청 전 확인 단계까지 연결하는 것이 목표입니다.
    </p>
    <div class="hs-keywords">
      <strong>추천 검색 키워드</strong>
      <span>임신 지원금, 출산 지원금, 육아 지원정책, 서울시 육아 지원, 부모급여, 아동수당, 아이돌봄, 생애주기 정책</span>
    </div>
  </div>
</section>

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
        <a class="btn btn--light-outline" href="https://play.google.com/store/apps/details?id=com.suimworks.hscode_assistant">Google Play</a>
        <a class="btn btn--light-outline" href="/hs-finder/privacy-policy/">개인정보처리방침</a>
      </div>
      <p>
        Android 앱은 Google Play에서 다운로드할 수 있습니다. iOS는 아직 지원하지 않습니다.
      </p>
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

<section class="tarot-showcase" id="onulmaum-tarot">
  <div class="tarot-showcase__hero">
    <div class="tarot-showcase__copy">
      <p class="page-chip">오늘의 마음 타로</p>
      <h2>마음이 복잡한 날, 카드로 가볍게 정리해보는 온라인 타로</h2>
      <p>
        오늘의 마음 타로는 연애 타로, 연락운 타로, 재회 타로, 고백 타로, 오늘의 운세 타로처럼 자주 궁금해지는 주제를
        한국어 리딩으로 정리해주는 웹 서비스입니다. Google 로그인 후 기본 리딩을 하루 3회 무료로 볼 수 있고,
        더 자세한 설명이 필요할 때만 AI 타로 해석을 선택할 수 있습니다.
      </p>
      <div class="tarot-showcase__actions">
        <a class="btn btn--primary" href="https://www.onulmaumtarot.kr">서비스 바로가기</a>
        <a class="btn btn--light-outline" href="#onulmaum-tarot-how-to">사용 방법 보기</a>
        <a class="btn btn--light-outline" href="#onulmaum-tarot-blog-kit">블로그 홍보 문구</a>
      </div>
      <div class="tarot-stats" aria-label="오늘의 마음 타로 요약">
        <span><strong>78장</strong> 메이저와 마이너 카드 기반 리딩</span>
        <span><strong>하루 3회</strong> Google 로그인 후 기본 리딩 무료</span>
        <span><strong>AI 해석</strong> 필요할 때만 추가로 자세한 리딩</span>
      </div>
    </div>
    <div class="tarot-phone" aria-label="오늘의 마음 타로 화면 예시">
      <div class="tarot-phone__bar">
        <strong>오늘의 마음 타로</strong>
        <span>연애, 연락, 재회, 오늘의 운세</span>
      </div>
      <div class="tarot-card-fan">
        <img src="{{ '/assets/images/onulmaum-tarot/card-back.png' | relative_url }}" alt="">
        <img src="{{ '/assets/images/onulmaum-tarot/the-star.png' | relative_url }}" alt="별 카드 예시">
        <img src="{{ '/assets/images/onulmaum-tarot/card-back.png' | relative_url }}" alt="">
      </div>
      <div class="tarot-phone__panel">
        <span>오늘의 질문</span>
        <p>지금 내 마음에 필요한 조언은?</p>
      </div>
      <div class="tarot-phone__panel">
        <span>리딩 결과</span>
        <p>상황을 단정하지 않고, 지금 살펴볼 포인트를 부드럽게 정리합니다.</p>
      </div>
    </div>
  </div>

  <div class="tarot-showcase__notice">
    <strong>이용 안내</strong>
    <span>
      타로 리딩은 자기성찰과 엔터테인먼트를 위한 참고 콘텐츠입니다. 의료, 법률, 투자, 정신건강처럼 중요한 의사결정은
      관련 전문가와 상의하는 것을 권장합니다.
    </span>
  </div>

  <div class="tarot-showcase__section">
    <div class="section-heading">
      <p class="page-chip">Blog Title Ideas</p>
      <h2>네이버 블로그에 쓰기 좋은 제목</h2>
    </div>
    <div class="tarot-promo-grid">
      <article>
        <h3>연락운이 궁금한 날</h3>
        <p>연락 기다리다 마음 복잡할 때, 온라인 타로로 가볍게 정리해보기</p>
      </article>
      <article>
        <h3>무료 타로 후기형</h3>
        <p>Google 로그인 후 하루 3회 무료, 오늘의 마음 타로 사용해본 느낌</p>
      </article>
      <article>
        <h3>연애 고민형</h3>
        <p>썸, 재회, 고백 고민을 한 번에 볼 수 있는 온라인 타로 사이트</p>
      </article>
      <article>
        <h3>오늘의 운세형</h3>
        <p>출근 전 1분, 오늘의 운세 타로로 마음 정리하는 방법</p>
      </article>
    </div>
  </div>

  <div class="tarot-showcase__section" id="onulmaum-tarot-how-to">
    <div class="section-heading">
      <p class="page-chip">How To Use</p>
      <h2>사용 방법은 간단합니다</h2>
    </div>
    <ol class="tarot-steps">
      <li>
        <strong>사이트에 접속합니다.</strong>
        브라우저에서 <a href="https://www.onulmaumtarot.kr">www.onulmaumtarot.kr</a> 주소로 들어갑니다.
      </li>
      <li>
        <strong>보고 싶은 주제를 고릅니다.</strong>
        오늘의 타로, Yes/No 타로, 연애 3카드, 연락운, 재회, 고백, 직장운, 금전운 등 상황에 맞는 메뉴를 선택합니다.
      </li>
      <li>
        <strong>질문을 떠올리고 카드를 선택합니다.</strong>
        “지금 내가 먼저 연락해도 괜찮을까?”처럼 구체적인 질문으로 시작하면 리딩을 더 쉽게 읽을 수 있습니다.
      </li>
      <li>
        <strong>기본 리딩 결과를 확인합니다.</strong>
        Google 로그인 후 기본 리딩은 하루 3회 무료로 볼 수 있습니다.
      </li>
      <li>
        <strong>필요할 때만 AI 해석을 추가합니다.</strong>
        기본 결과보다 더 자세한 설명이 필요할 때 AI 타로 해석을 선택하면 됩니다.
      </li>
    </ol>
  </div>

  <div class="tarot-showcase__section" id="onulmaum-tarot-blog-kit">
    <div class="section-heading">
      <p class="page-chip">Naver Blog Copy</p>
      <h2>블로그 홍보 본문 초안</h2>
      <p>아래 문구는 네이버 블로그 본문에 맞춰 다듬어 사용할 수 있도록 구성했습니다.</p>
    </div>
    <div class="tarot-copy">
      <p>
        마음이 복잡할 때는 누군가에게 바로 털어놓기도 어렵고, 혼자 계속 생각하다 보면 같은 고민만 반복하게 되는 것 같아요.
        그럴 때 가볍게 참고해볼 수 있는 온라인 타로 사이트로 <strong>오늘의 마음 타로</strong>를 소개해봅니다.
      </p>
      <p>
        오늘의 마음 타로는 연애 타로, 연락운 타로, 재회 타로, 고백 타로, 오늘의 운세 타로처럼 자주 궁금해지는 주제별 메뉴가
        따로 정리되어 있습니다. 질문을 고르고 카드를 선택하면 기본 리딩 결과를 볼 수 있고, Google 로그인 후에는 기본 리딩을
        하루 3회 무료로 이용할 수 있습니다.
      </p>
      <p>
        좋았던 점은 결과가 무조건적인 예언처럼 나오기보다, 지금 상황에서 어떤 부분을 차분히 봐야 하는지 정리해주는 느낌이라는 점입니다.
        특히 연락을 기다리거나, 썸인지 아닌지 헷갈리거나, 재회를 고민하는 상황에서는 마음을 한 번 정돈하는 데 도움이 됩니다.
      </p>
      <p>
        기본 리딩을 본 뒤 더 자세한 해석이 필요하면 AI 타로 해석도 선택할 수 있습니다. 꼭 필요한 기능은 아니지만,
        선택한 카드와 질문을 바탕으로 조금 더 긴 설명을 보고 싶을 때 사용하면 좋습니다.
      </p>
    </div>
  </div>

  <div class="tarot-showcase__section">
    <div class="section-heading">
      <p class="page-chip">Capture Frames</p>
      <h2>캡처해서 홍보 이미지로 쓰기 좋은 프레임</h2>
      <p>대표 이미지와 카드뉴스 느낌의 정사각형 프레임을 페이지 안에 함께 배치했습니다.</p>
    </div>
    <div class="tarot-capture-grid">
      <article>
        <div class="tarot-capture tarot-capture--wide">
          <div>
            <span>하루 3회 무료 기본 리딩</span>
            <h3>연락 기다리다 마음 복잡한 날</h3>
            <p>오늘의 마음 타로에서 카드 한 장으로 지금의 흐름을 가볍게 정리해보세요.</p>
          </div>
          <div class="tarot-capture__cards" aria-hidden="true">
            <img src="{{ '/assets/images/onulmaum-tarot/the-lovers.png' | relative_url }}" alt="">
            <img src="{{ '/assets/images/onulmaum-tarot/the-star.png' | relative_url }}" alt="">
            <img src="{{ '/assets/images/onulmaum-tarot/the-sun.png' | relative_url }}" alt="">
          </div>
        </div>
        <p>블로그 대표 이미지나 본문 상단 이미지로 사용하기 좋은 1200x630 계열 구성입니다.</p>
      </article>
      <article>
        <div class="tarot-capture tarot-capture--square">
          <span>오늘의 마음 타로</span>
          <h3>사용 방법은 간단해요</h3>
          <p>1. 주제 선택<br>2. 질문 떠올리기<br>3. 카드 선택<br>4. 기본 리딩 확인<br>5. 필요하면 AI 해석 추가</p>
          <small>www.onulmaumtarot.kr</small>
        </div>
        <p>블로그 본문 중간에 카드뉴스처럼 삽입하기 좋은 정사각형 구성입니다.</p>
      </article>
    </div>
  </div>

  <div class="tarot-showcase__section">
    <div class="section-heading">
      <p class="page-chip">Topics</p>
      <h2>주제별 메뉴 소개</h2>
    </div>
    <ul class="tarot-topic-list">
      <li>오늘의 타로: 하루의 흐름과 조언</li>
      <li>Yes / No 타로: 지금 질문의 현재 흐름</li>
      <li>연애 3카드: 현재 상황, 관계 흐름, 조언</li>
      <li>연락운 타로: 연락 가능성과 내가 취할 태도</li>
      <li>재회 타로: 과거 관계와 다시 연결될 가능성</li>
      <li>고백 타로: 고백 전 확인해볼 마음의 준비</li>
      <li>직장운 타로: 일과 커리어 방향</li>
      <li>금전운 타로: 이번 달 재정 흐름</li>
    </ul>
  </div>

  <div class="tarot-showcase__section">
    <div class="section-heading">
      <p class="page-chip">Hashtags</p>
      <h2>추천 해시태그</h2>
    </div>
    <ul class="tarot-tag-list">
      <li>#무료타로</li>
      <li>#온라인타로</li>
      <li>#오늘의타로</li>
      <li>#연애타로</li>
      <li>#연락운타로</li>
      <li>#재회타로</li>
      <li>#썸타로</li>
      <li>#고백타로</li>
      <li>#직장운타로</li>
      <li>#금전운타로</li>
      <li>#AI타로</li>
      <li>#타로사이트</li>
      <li>#타로후기</li>
      <li>#마음정리</li>
      <li>#오늘의마음타로</li>
    </ul>
  </div>

  <div class="tarot-showcase__cta">
    <strong>오늘 마음이 복잡하다면, 무료 타로로 가볍게 정리해보세요.</strong>
    <span>오늘의 마음 타로에서 기본 리딩을 하루 3회 무료로 볼 수 있습니다.</span>
    <a class="btn btn--primary" href="https://www.onulmaumtarot.kr">오늘의 마음 타로 보러가기</a>
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
