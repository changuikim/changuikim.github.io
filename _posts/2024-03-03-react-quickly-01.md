---
title: "[React] - React Quickly 1"
layout: single
tags: ["Book Review", "React Quickly Second Edition", "Frontend"]
categories: ["React"]
date: "2024-03-03 23:10:10 +0900"
last_modified_at: "2024-03-04 20:20:00 +0900"
---

React Quickly Second Edition 1장을 읽고나서

# 1.1 리액트의 특징

- 선언형 프로그래밍과 순수한 자바스크립트만을 사용하기에 단순함에서 오는 이점이 있다.
- 가상 DOM과 DOM의 차이가 있는 부분만을 선택적으로 렌더링하기에 효율적이다.
- 단방향 바인딩만 제공하고 다양한 의존성 패키지를 관리해야할 필요성이 있다.
- 백엔드 프레임워크의 종류에 영향을 받지 않는다.

# 1.2 JSX 없이 React 애플리케이션 생성하기

- [https://react.dev/reference/react/createElement#creating-an-element-without-jsx](https://react.dev/reference/react/createElement#creating-an-element-without-jsx)

## 1.2.1 React Core 라이브러리

- 전역객체 window.React에 엑세스할 수 있다.
- createElement(type , props , …children) 메서드
    - [https://react.dev/reference/react/createElement#createelement](https://react.dev/reference/react/createElement#createelement)
    - type, props와 children을 사용해 리액트 엘리먼트를 생성한다.
    
    ```jsx
    import { createElement } from 'react';
    
    function Greeting({ name }) {
      return createElement(
        'h1',
        { className: 'greeting' },
        'Hello'
      );
    }
    ```
    
    - Parameters
        - type : 리액트 컴포넌트 타입
        - props : 객체 또는 null
        - …children : 없거나 1개 이상의 리액트 노드
    - Returns
        - type, props, ref, key 등의 프로퍼티를 가진 리액트 엘리먼트 객체를 반환한다.

## 1.2.2 React DOM 라이브러리

- 전역객체 window.ReactDom에 엑세스 할 수 있다.
- createRoot(domNode, options?) 메서드
    - [https://react.dev/reference/react-dom/client/createRoot#createroot](https://react.dev/reference/react-dom/client/createRoot#createroot)
    - 브라우저 DOM 엘리먼트 안의 컨텐트를 표시하기 위한 리액트 루트를 생성한다.
    
    ```jsx
    import { createRoot } from 'react-dom/client';
    
    const domNode = document.getElementById('root');
    const root = createRoot(domNode);
    ```
    
    - Parameters
        - domNode : DOM 엘리먼트
        - options : 없거나 onRecoverableError, identifierPrefix 등
    - Returns
        - render와 unmount 메서드를 가지는 객체를 반환한다.
- root.render(reactNode) 메서드
    - [https://react.dev/reference/react-dom/client/createRoot#root-render](https://react.dev/reference/react-dom/client/createRoot#root-render)
    - 리액트 루트의 브라우저 DOM 노드 안에 리액트 노드의 조각을 표시한다.
    
    ```jsx
    root.render(<App />);
    ```
    
    - Parameters
        - reactNode : 표시하고자하는 리액트 노드
    - Returns
        - undefined를 반환한다.

## 1.2.3 JSX 없이 React 애플리케이션 만들기

```html
<!DOCTYPE html>
<html>
  <head>
    <title>JSX 없이 React 애플리케이션 만들기</title>
    <script src="//unpkg.com/react@18/umd/react.development.js"></script> 
    <script src="//unpkg.com/react-dom@18/umd/react-dom.development.js"></script>
  </head>
  <body>    
    <div id="root"></div>
    <script type="text/javascript">
      ReactDOM        
        .createRoot(document.getElementById('root'))        
        .render(React.createElement('h1', null, 'Hello World'));            
    </script>
  </body>
</html>
```

- React Core, ReactDOM 라이브러리의 React 18 버전에 대한 링크를 사용했다.
- createRoot 메서드를 사용해 id가 root인 브라우저 DOM 엘리먼트를 표시하기 위한 리액트 루트를 생성한다.
- createElement 메서드를 사용해 h1 타입의 Hello World 문자열을 자식 노드로 가지는 리액트 컴포넌트를 생성한다.
- render 메서드를 사용해 리액트 루트의 브라우저 DOM 노드 안에 리액트 컴포넌트를 표시한다.
