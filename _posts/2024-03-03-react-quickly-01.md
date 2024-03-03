---
title: "[React] - React Quickly 1장"
layout: single
date: "2024-03-03 23:10:10 +0900"
last_modified_at: "2024-03-03 23:10:10 +0900"
categories: ["React", "Review"]
tags: ["React Quickly"]
---

## 01 리액트의 특징

- 선언형 프로그래밍과 순수한 자바스크립트만을 사용하기에 단순함에서 오는 이점이 있다.
- 가상 DOM과 DOM의 차이가 있는 부분만을 선택적으로 렌더링하기에 효율적이다.
- 단방향 바인딩만 제공하고 다양한 의존성 패키지를 관리해야할 필요성이 있다.
- 백엔드 프레임워크의 종류에 영향을 받지 않는다.

## 02 JSX 없이 React 애플리케이션 만들기

```html
<!DOCTYPE html>
<html>
  <head>
    <title>JSX 없이 React 애플리케이션 만들기</title>
    <script src="//unpkg.com/react@18/umd/react.development.js"></script> 
    <script src="//unpkg.com/react-dom@18/umd/react-dom.development.js"></script>
  </head>
  <body>    
    <div id="DOM-element"></div>
    <script type="text/javascript">
      ReactDOM        
        .createRoot(document.getElementById('DOM-element'))        
        .render(React.createElement('p', null, 'Hello World'));            
    </script>
  </body>
</html>
```

- React Core 라이브러리를 사용하면 전역객체 window.React에 접근할  수 있다.
    - createElement(’요소’, ‘요소 속성’, ‘자식 요소’) 메서드를 사용하여 React 컴포넌트를 인스턴스화한다.
- React DOM 라이브러리를 사용하면 전역객체 window.ReactDOM에 접근할 수 있다.
    - createRoot(DOM 요소) 메서드를 사용하여 리액트 애플리케이션 루트 홀더를 생성한다.
    - 리액트 애플리케이션 루트 홀더에 render(리액트 요소) 메서드를 사용하여 리액트 컴포넌트를 렌더링한다.
