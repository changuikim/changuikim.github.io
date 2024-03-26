---
title: "[BookReview] 리액트 with 타입스크립트 01"
layout: single
tags:
    - Frontend
    - JavaScript
    - TypeScript
    - React  
categories:
    - BookReview
date: 2024-03-24 18:47:00 +0900
last_modified_at: 2024-03-24 19:37:00 +0900
---
현장에서 바로 써먹는 리액트 with 타입스크립트 01장을 읽고나서

# 1 다루는 내용

- 웹(Web)의 역사
- 리액트(React)의 탄생
- 리액트의 특징
- 리액트의 현재와 장래성

# 2 알게된 점

## 2.1 자바스크립트의 등장

- 자바스크립트 언어를 처음 개발한 건 넷스케이프 커뮤니테션즈 Netscape Communications였다.
- Hyper Text Markup Language (HTML)은 팀 버너스리 Tim Berners-Lee가 CERN 연구소에서 1990년 개발하였다.
- 팀 버너스리는 이를 누구나 열람할 수 있도록 HTTP를 개발하였으며, 최초의 정적인 웹 브라우저 월드와이드웹도 개발하였다.
- 넷스케이프 내비게이터 Netscape Navigator의 개발 코드명이 모질라 Mosaic and Godzilla였다.
- 넷스케이프가 시장 점유율 90%에 달할때 동적인 프로그래밍 언어를 개발한 것이 자바스크립트 JavaScript이다.
- 마이크로소프트 Microsot에서도 자바스크립트와 호환이 가능한 JScript라는 언어를 만들었지만, 점차 언어 간에 차이가 생기기 시작했다.
- 넷스케이프가 1996년 비영리 표준화 기구인 ECMA 인터네셔널에 자바스크립트 표준화를 요청하였고, 1997년 자바 스크립트 초판 명세서인 ECMA-262가 완성되었다. 이를 ECMAScript라고 명명한다.

## 2.2 리액트의 등장

- 크로스 브라우징 문제는 여전히 해결되지 않아서 2006년 등장한  jQuery가 사실상 표준이 되었다.
- XMLHttpRequest API는 1999년 IE5에서 소개되었다.
- JSON은 2001년 더글라스 크락포드 Douglas Crockfor에 의해 소개되었다.
- Asynchronous JavaScript And XML (Ajax)는 2004년 구글에 의해 사용되었다.
- 웹 서비스에서도 애플리케이션 Application이라는 개념이 대중적으로 사용된건 2007년부터이다.
- AngularJS는 구글이 웹 애플리케이션 트렌드에 대응하고자 2010년에 출시하였다.
- Single Page Application (SPA) 개념은 AngularJS의 등장과 함께 시작되었다.
- React는 페이스북의 개발자 조던 워크 Jordan Walke가 2011년 처음 개발하였다. 2013년 페이스북이 리액트를 오픈 소스로 발표하였다.
- AngularJS는 싱글 페이지 애플리케이션 프레임워크이지만 React는 싱글 페이지 애플리케이션의 UI 자바스크립트 라이브러리이다. 즉, User Interface (UI) 에 집중한 라이브러리이다.
- 가상 돔 Virtual DOM 개념은 리액트와 함께 등장하였다.
- 리액트는 부족한 부분을 채우기 위해 다른 라이브러리를 쓰거나 리액트 프레임워크를 써야한다.

## 2.3 리액트의 특징

- 리액트는 JavaScript XML라는 템플릿 언어를 사용한다.
- 리액트는 단방향 데이터 바인딩을 사용하므로, 이벤트를 통해 명시적으로 데이터를 갱신한다.
	- Angular와 Vue는 양방향 데이터 바인딩을 사용하므로, 데이터를 자동으로 동기화한다.
- 리액트는 가상 돔을 사용해 SPA의 성능 최적화를 이뤄냈다.
	- 브라우저는 렌더 엔진을 통해 HTML을 파싱하여 DOM Node로 구성된 트리를 만들며, CSS를 파싱해 스타일 정보를 가진 트리를 만든다.
	- Attachment를 통해 화면에 표시될 부분을 계산한 후, Render Tree를 만들며 Layout과 Painting을 거쳐서 화면에 내용을 표시하게 된다.
	- 자바스크립트를 통해 돔 트리를 조작하면 동기적으로 레이아웃이 다시 수행되는 Reflow와 페인팅이 다시 수행되는 Repaint가 발생한다.
	- 리액트는 메모리 상에 동일한 돔 트리를 생성해서 모든 연산을 마친 후 브라우저 상의 돔 트리에 반영하는 방식으로 리플로와 리페인트의 연산을 최소화했다.
- 리액트는 선언형 프로그래밍을 활용해 How보다는 What에 집중하여 코드를 구현한다.
- 리액트는 컴포넌트 단위로 코드를 구성하고 재사용한다.

# 3 관련 링크

- https://microsoft.github.io/reactxp/

- https://github.com/facebook/react/

- https://reactnative.dev/