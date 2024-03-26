---
title: "[GitHub Pages] - 3 Pages 만들기"
layout: single
tags:
    - Blog
categories: 
    - GitHubPages
date: 2024-03-02 21:24:11 +0900
last_modified_at: 2024-03-26 23:43:00 +0900
---
_config.yml 파일 수정, About 페이지 추가, 404 페이지 추가

# 1 Jekyll 설정 파일에 페이지 관련 설정을 추가

## 1.1 Default 설정을 추가

- scope
    - path: 스코프를 적용할 경로
    - type: 스코프를 적요할 타입
- value
    - layout: 레이아웃
    - author_profile: 사이드바에 프로필을 표시
    - read_time: 포스트 완독 추측 시간을 표시
    - comments: 댓글 표시
    - share: 소셜 공유 기능
    - related: 관련 포스트 추천
    - toc: 현재 페이지의 목차 표시

## 1.2 포스트별로 적용 가능한 프로퍼티

- title: 포스트 제목
- layout: 레이아웃
- permalink: 서브 경로
- date: 만든 날짜
- last_modified_at: 수정 날짜
- categories: 카테고리
- tags: 태그

# 2 날짜 정보와 상관없는 페이지 포스트를 추가

## 2.1 About 페이지

```markdown
---
title: "changuikim의 개발자 블로그"
permalink: /about/
layout: single
---

- 웹 개발과 관련된 지식과 생각을 기록하는 블로그입니다.
- JavaScript와 React를 사용해 프론트엔드 개발을 합니다.
- Java와 Spring을 사용해 백엔드 개발을 합니다.
- Node.js를 사용해 백엔드 개발을 합니다.
```

## 2.2 404 에러 페이지

```markdown
---
title: "404 Page Not Found"
excerpt: "Page not found. Your pixels are in another canvas."
permalink: /404.html
author_profile: false
---

요청하신 페이지를 찾을 수 없습니다.

<script>
  var GOOG_FIXURL_LANG = 'en';
  var GOOG_FIXURL_SITE = 'https://changuikim.github.io';
</script>
<script src="https://linkhelp.clients.google.com/tbproxy/lh/wm/fixrul.js">
</script>
```