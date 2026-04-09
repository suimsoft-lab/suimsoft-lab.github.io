# suimsoft-lab.github.io

`suimsoft-lab`의 GitHub Pages 기반 Jekyll 블로그입니다.  
앱 개발 과정 기록과 배포 후 운영 안내 문서를 정리합니다.

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
