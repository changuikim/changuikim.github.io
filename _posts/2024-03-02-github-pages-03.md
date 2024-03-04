---
title: "[GitHub Pages] - 3 Pages 만들기"
layout: single
tags: ["Blog"]
categories: ["GitHub Pages"]
date: "2024-03-02 21:24:11 +0900"
last_modified_at: "2024-03-04 21:26:00 +0900"
---

생성 날짜에 영향받지 않는 페이지를 생성하기

# 1 Default 설정 추가

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

# 2 포스트별 적용하는 옵션

- title: 포스트 제목
- layout: 레이아웃
- permalink: 서브 경로
- date: 만든 날짜
- last_modified_at: 수정 날짜
- categories: 카테고리
- tags: 태그

# 3 About 페이지 추가

- 블로그 소개글

```markdown
---
title: "Changui Kim의 개발자 블로그"
permalink: /about/
layout: single
---

## Changui Kim의 개발자 블로그

- 웹 개발을 하며 생각과 고민을 기록하는 블로그입니다.  
- SpringFramework를 사용해 웹 애플리케이션을 개발합니다.
- Node.js를 사용해 웹 애플리케이션을 개발합니다.
- React를 사용해 싱글 페이지 애플리케이션을 개발합니다.
- Java, Python을 사용해 자료구조와 알고리즘을 공부합니다.
```

# 4 404 페이지 추가

- 404 Not Found 오류에 대응할 페이지

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