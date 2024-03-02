---
title: "[GitHub Pages] - 4 상단 메뉴 구성하기"
layout: single
date: "2024-03-02 21:59:54 +0900"
last_modified_at: "2024-03-02 21:59:54 +0900"
categories: ["GitHub Pages"]
tags: ["GitHub Pages"]
---

# 1 _config.yml 수정하기

- Archives에 type과 path를 설정

# 2 _data/navigation.yml 수정하기

- main에 title과 url을 설정

# 3 카테고리 페이지 만들기

- category-archive.md

```
---
title: "Posts by Category"
layout: categories
permalink: /categories/
author_profile: true
---
```

# 4 태그 페이지 만들기

- tag-archive.md

```
---
title: "Posts by Tag"
permalink: /tags/
layout: tags
author_profile: true
---
```

# 5 CSS 수정

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