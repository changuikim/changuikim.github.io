---
title: "[GitHub Pages] - 4 상단 메뉴 구성하기"
layout: single
tags:
    - Blog
categories: 
    - GitHub Pages
date: 2024-03-02 21:59:54 +0900
last_modified_at: 2024-03-26 23:49:00 +0900
---

# 1 Jekyll 설정 파일에 상단 메뉴 관련 설정을 추가

## 1.1 _config.yml 수정

- Archives에 type과 path를 설정한다.

## 1.2 _data/navigation.yml 수정

- main에 title과 url을 설정한다.

# 2 상단 메뉴 관련 페이지 포스트 추가

## 2.1 Category 페이지

```
---
title: "Posts by Category"
layout: categories
permalink: /categories/
author_profile: true
---
```

## 2.2 Tag 페이지

```
---
title: "Posts by Tag"
permalink: /tags/
layout: tags
author_profile: true
---
```

# 3 화면 비율 조정을 위해 CSS를 수정

- *_sass/minimal-mistakes/*_reset.scss에서 htm 폰트 조절

  ```
  html {
    /* apply a natural box layout model to all elements */
    box-sizing: border-box;
    background-color: $background-color;
    font-size: 16px;

    // @include breakpoint($medium) {
    //   font-size: 18px;
    // }

    // @include breakpoint($large) {
    //   font-size: 20px;
    // }

    // @include breakpoint($x-large) {
    //   font-size: 22px;
    // }

    -webkit-text-size-adjust: 100%;
    -ms-text-size-adjust: 100%;
  }
  ```

- *_sass/minimal-mistakes/_variables.scss에서 Grid 사이드바 조절*

  ```
  /*
    Grid
    ========================================================================== */

  $right-sidebar-width-narrow: 100px !default; // 200px
  $right-sidebar-width: 200px !default; // 300px
  $right-sidebar-width-wide: 250px !default; // 400px
  ```