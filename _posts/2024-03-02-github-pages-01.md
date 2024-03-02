---
title: "[GitHub Pages] - 1 Jekyll Theme을 사용해 블로그 생성하기"
layout: single
date: "2024-03-02 20:41:12 +0900"
last_modified_at: "2024-03-02 20:41:12 +0900"
categories: ["GitHub Pages"]
tags: ["GitHub Pages"]
---

# 1 개발 환경 구축하기

## 1) Ruby

- [https://rubyinstaller.org/downloads/](https://rubyinstaller.org/downloads/)에서 Ruby+Devkit 3.2.3-1 (x64) 설치

## 2) Jekyll

```bash
gem install jekyll bundler
```

## 3) VSCode

- Markdown All in One 확장

## 4) GitHub Pages 저장소 생성하기

[https://github.com/changuikim/changuikim.github.io](https://github.com/changuikim/changuikim.github.io)

# 2 Jekyll Theme 를 사용해 블로그 생성하기

## 1) minimal-mistakes 클론하기

[https://github.com/mmistakes/minimal-mistakes](https://github.com/mmistakes/minimal-mistakes)

```bash
# mmistakes 저장소 클론
git clone git@github.com:mmistakes/minimal-mistakes.git
```

## 2) Quick-Start Guide에 따라 불필요한 소스 삭제하기

- 디렉토리
    - .git
    - docs
    - test
- 파일
    - screenshot.png
    - screenshot-layouts.png

## 3) 샘플 블로그 생성해서 확인하기

```bash
# 샘플 블로그 생성 및 확인하기
cd minimal-mistakes
bundle
bundle exec jekyll serve
```

# 3 저장소에 push해서 GitHub Pages 웹호스팅 하기

```bash
# 내 저장소에 push 하기
git remote add origin git@github.com:changuikim/changuikim.github.io.git
git commit
git branch -M main
git push -u origin main
```