---
title: "[BookReview] 리액트 with 타입스크립트 02"
layout: single
tags:
  - Frontend
  - JavaScript
  - TypeScript
  - React
categories:
  - BookReview
date: 2024-03-24 20:58:00 +0900
last_modified_at: 2024-03-24 21:32:00 +0900
---
현장에서 바로 써먹는 리액트 with 타입스크립트 02장을 읽고나서

# 1 다루는 내용

- Chocolatey 설치
- Node.js 설치
- 리액트 프로젝트를 설치하는 방법

# 2 알게된 점

## 2.1 Chocolatey

- 윈도우 환경에서도 소프트웨어 관리를 자동화하는 Package Manager가 있었다.
	- https://docs.chocolatey.org/en-us/
- 설치 페이지에서 Individual Use를 위한 설치 명령어를 복사해 Power Shell에서 실행하면 설치가 가능한다.
	- https://chocolatey.org/install#install-step2
	- 설치를 위해서는 PowerShell v2+와 .Net Framework 4.8이 필요하다.
- 다른 프로그램과 마찬가지로 CMD에서 버전 확인이 가능하다.
	```
	choco -version
	```
## 2.2 Node.js

- 리액트는 자바스크립트 라이브러리이기 때문에 외부 라이브러리 사용을 위해 노드의 NPM을 사용할 수 있다.
- Node.js 홈페이지에서 설치가 가능하다. 현재 LTS 버전은 v20.11.1이다.
	- https://nodejs.org/en
- 초콜리티를 활용해 노드를 설치할 수도 있다.
	```
	choco install -y nodejs.install
	```
 - 다른 프로그램과 마찬가지로 CMD에서 버전 확인이 가능하다.
	```
	node --version
	npm --version
	```

## 2.3 리액트 프로젝트를 설치하는 방법

- 스크립트 태그를 사용해 리액트 라이브러리를 사용한다.
	```
	unpkg.com/react@18/umd/react.production.min.js
	unpkg.com/react-dom@18/umd/react-dom.production.min.js
	```
	- https://unpkg.com/ 사이트에서 npm에 존재하는 라이브러리를 사용할 수 있다.

- React Create App을 사용한다.
	```
	npx create-react-app my-app
	cd my-app
	npm start
	```
	- https://create-react-app.dev/
	- https://github.com/facebook/create-react-app

- Next.js를 사용한다.
	- https://nextjs.org/

## 2.4 Create React App

- create-react-app으로 생성된 리액트 프로젝트 디렉토리 구조

	```
	my-app
	├── README.md
	├── node_modules
	├── package.json
	├── .gitignore
	├── public
	│   ├── favicon.ico
	│   ├── index.html
	│   └── manifest.json
	└── src
	    ├── App.css
	    ├── App.js
	    ├── App.test.js
	    ├── index.css
	    ├── index.js
	    ├── logo.svg
	    └── serviceWorker.js
	    └── setupTests.js
	```
- public 폴더에는 웹 페이지의 정적인 부분과 관련된 파일이 들어있다.
- src 폴더에는 웹 페이지의 동적인 부분과 관련된 파일이 들어있다.
- node_modules에는 의존성 패키지가 들어있다.
- package.json 파일은 프로젝트 상세를 나타낸다.