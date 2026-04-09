# suimsoft-lab.github.io

`suimsoft-lab`의 GitHub Pages 기반 Jekyll 블로그입니다.  
앱 개발 과정, 기능 개선 기록, 배포 후 사용자 안내 문서를 정리합니다.

![Jekyll](https://img.shields.io/badge/Jekyll-3.10.0-CC0000?logo=jekyll&logoColor=white)
![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-deployed-222222?logo=githubpages&logoColor=white)
![Ruby](https://img.shields.io/badge/Ruby-3.x-CC342D?logo=ruby&logoColor=white)

## 프로젝트 앱

### 아기첫걸음

출산 직후 필요한 행정 절차/지원금 신청 일정을 한눈에 관리할 수 있는 앱입니다.

[![Google Play에서 보기](https://play.google.com/intl/en_us/badges/static/images/badges/ko_badge_web_generic.png)](https://play.google.com/store/apps/details?id=com.babyfirststep.baby_first_step)

### 아이지원

임신·출산·육아 단계별 지원정책을 지역/시기 기준으로 확인할 수 있는 앱입니다.

[![Google Play에서 보기](https://play.google.com/intl/en_us/badges/static/images/badges/ko_badge_web_generic.png)](https://play.google.com/store/apps/details?id=com.suimworks.babysupport)

## 로컬 실행

사전 준비:
- Ruby 3.x
- Bundler (`gem install bundler`)

실행:

```bash
bundle install
bundle exec jekyll serve
```

브라우저에서 `http://127.0.0.1:4000` 접속

## 글 작성 방법

1. `_posts/` 경로에 `YYYY-MM-DD-title.md` 파일 생성
2. 파일 상단 Front Matter 작성:

```yaml
---
layout: post
title: "글 제목"
date: 2026-04-09 09:00:00 +0900
categories: [devlog]
tags: [flutter, android]
---
```

3. 본문 작성 후 커밋/푸시

## 배포

`main` 브랜치에 푸시하면 GitHub Pages가 자동 빌드/배포합니다.

## 참고

- 블로그 주소: <https://suimsoft-lab.github.io>
- GitHub 계정: <https://github.com/suimsoft-lab>
