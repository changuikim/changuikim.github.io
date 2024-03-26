---
title: "[GitHub Pages] - 1 Jekyll Theme을 사용해 블로그 생성하기"
layout: single
tags:
    - Blog
categories: 
    - GitHub Pages
date: 2024-03-02 20:41:12 +0900
last_modified_at: 2024-03-26 23:08:00 +0900
---
개발 환경 구축하기, Jeykyll 블로그 생성하기, 블로그 호스팅하기

# 1 개발 환경 구축하기
## 1.1 Ruby
- Jekyll을 사용하기 위해 [Ruby+Devkit 3.2.3-1 (x64)](https://rubyinstaller.org/downloads/)를 설치한다.

## 1.2 Jekyll
- Ruby 언어의 패키지 관리자인 RubyGems를 사용하여 jekyll과 bundler를 설치한다.
    ```bash
    gem install jekyll bundler
    ```

## 1.3 마크다운 편집기
### 1.3.1 Notion
- 온라인 마크다운 편집기로 많이 사용하는 [Notion](https://www.notion.so/)을 사용한다.

### 1.3.2 Obsidian
- 로컬 마크다운 편집기로 많이 사용하는 [Obsidian](https://obsidian.md/)을 사용한다.

### 1.3.3 VSCode의 Extension
- [Visual Studio Code](https://code.visualstudio.com/)를 설치하고 마크다운 관련 확장을 설치한다.
- Markdown All in One 을 사용하였다.

## 1.3.4 GitHub Pages 저장소 생성하기
- 사용자 이름을 사용한 깃허브 저장소는 특별한 의미를 지닌다. 여기에 github.io를 추가해 GitHub Pages에 연동되는 저장소를 생성하였다.
- [changuikim.github.io](https://github.com/changuikim/changuikim.github.io) 저장소

# 2 Jekyll Theme 를 사용해 블로그 생성하기
## 2.1 minimal-mistakes 클론하기
- Jeykyll Theme 중에서 가장 많이 사용되는 Minimal Mistakes를 사용하였다.
- [minimal-mistakes](https://github.com/mmistakes/minimal-mistakes) 저장소를 클론하거나 zip 파일로 내려받아 사용할 수 있다.
    ```bash    
    git clone git@github.com:mmistakes/minimal-mistakes.git
    ```

## 2.2 Quick-Start Guide에 따라 불필요한 소스 삭제하기
- [minimal-mistakes](https://github.com/mmistakes/minimal-mistakes) 저장소에서 제공하는 README.md 문서에서 삭제해도 되는 디렉토리와 파일을 알려주고 있다.
- 디렉토리
    - .git
    - docs
    - test
- 파일
    - screenshot.png
    - screenshot-layouts.png

## 2.3 샘플 블로그 생성해서 로컬에서 블로그 실행하기
- bundle 명령어를 사용해 샘플 블로그를 생성하고 이를 로컬에서 실행할 수 있다.
    ```bash    
    cd minimal-mistakes
    bundle # 샘플 블로그를 생성한다.
    bundle exec jekyll serve # 로컬에서 블로그를 실행한다.
    ```
- 생성된 블로그는 동일한 명령어를 사용해 로컬에서 실행 테스트가 가능하다.
    ```bash
    bundle exec jekyll serve
    ```
- 실행된 블로그는 [4000번 포트](http://localhost:4000/)에서 접속 가능하다.
    ```bash
    Server address: http://127.0.0.1:4000
    Server running... press ctrl-c to stop.
    ```

# 3 저장소에 push해서 GitHub Pages 웹호스팅 하기
- 사용자 이름을 사용한 [changuikim.github.io](https://github.com/changuikim/changuikim.github.io) 저장소에 Jeykyll 소스 코드를 푸시하면 GitHub가 이를 자동으로 Pending하고 오류가 없다면 Deploy까지 진행한다. 
    ```bash    
    git remote add origin git@github.com:changuikim/changuikim.github.io.git
    git commit
    git branch -M main
    git push -u origin main
    ```
- 저장소 이름 [changuikim.github.io](https://changuikim.github.io)으로 접속하면 블로그가 호스팅 중인 것을 확인할 수 있다.
