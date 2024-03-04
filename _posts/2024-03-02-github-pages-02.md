---
title: "[GitHub Pages] - 2 Minimal Mistakes 환경설정"
layout: single
tags: ["Blog"]
categories: ["GitHub Pages"]
date: "2024-03-02 20:47:25 +0900"
last_modified_at: "2024-03-04 20:25:00 +0900"
---

Jekyll 테마로 생성한 샘플 블로그를 _config.yml을 수정해서 커스터마이징

# 1 Site Settings

- locale
    - 사이트의 주 언어
    - “en-US” → “ko-KR”
- title
    - 사이트의 이름
    - “Site Title” → “Changuikim의 개발 블로그”
- subtitle
    - 사이트의 이름 아래에 표시되는 짧은 태그라인
    - → “Version 0.1”
- name
    - 사이트 저자의 이름
    - “Your Name” → “Changui Kim”
- description
    - 사이트 설명
    - “An amazing website” → “웹 개발을 하며 생각과 고민을 기록하는 블로그”
- url
    - 사이트의 호스트 네임
    - → “https://changuikim.github.io”
- repository
    - → “https://github.com/changuikim/changuikim.github.io”

# 2 Site Author

- 사이드바에 표시되는 개발자 정보
- name
    - “Your Name” → “Changui Kim”
- bio
    - “I am an amazing person.” → “신입 웹 개발자”
- location
    - “Somewhere” → “Republic of Korea”
- Email
    - url: “mailto:cu.kim.dev@gmail.com”
- GitHub
    - url: “https://github.com/changuikim”

# 3 Site Footer

- 하단바에 표시되는 저자 정보
- GitHub
    - url: “https://github.com/changuikim”

# 4 Outputting

- 블로그 표시 방법
- paginate
    - 한 페이지에 노출 될 게시글 수
    - 5 → 15

# 5 Defaults

## 1) _posts

- 날짜를 기반으로 한 블로그 포스트
    - type: posts
    - read_time: true
    - comments: true
    - related: true

## 2) _pages

- 날짜와 관련없는 블로그 페이지
    - type: pages
    - read_time: false
    - comments: false
    - related: false