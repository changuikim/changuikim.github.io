---
title: "[React] - React Quickly 2"
layout: single
tags: ["Book Review", "React Quickly Second Edition", "Frontend"]
categories: ["React"]
date: "2024-03-04 23:55:28 +0900"
last_modified_at: "2024-03-05 10:24:00 +0900"
---

React Quickly Second Edition 2장을 읽고나서

# 2.1 Create React App을 사용하여 리액트 프로젝트 생성하기

- [https://create-react-app.dev/](https://create-react-app.dev/)
- Node > = 14부터 로컬에서 리액트 애플리케이션을 생성 가능하다.
    
    ```bash
    # npm 5.2+
    npx create-react-app my-app
    
    # npm 6+
    npm init react-app my-app
    ```
    
    ```bash
    # 디렉토리 구조
    my-app
    ├── README.md
    ├── node_modules
    ├── package.json
    ├── .gitignore
    ├── public
    │   ├── favicon.ico
    │   ├── index.html
    │   ├── logo192.png
    │   ├── logo512.png
    │   ├── manifest.json
    │   └── robots.txt
    └── src
        ├── App.css
        ├── App.js
        ├── App.test.js
        ├── index.css
        ├── index.js
        ├── logo.svg
        ├── serviceWorker.js
        └── setupTests.js
    ```
    
- 옵션을 추가해 템플릿이 적용된 리액트 애플리케이션을 생성 가능하다.
    
    ```bash
    npx create-react-app my-app --template [template-name]
    ```
    
    - [https://www.npmjs.com/search?ranking=popularity&q=cra-template-*](https://www.npmjs.com/search?ranking=popularity&q=cra-template-*)

# 2.2 클래스 컴포넌트 정의해서 사용하기

- [https://react.dev/reference/react/Component#defining-a-class-component](https://react.dev/reference/react/Component#defining-a-class-component)
- CHILD extends PARENT의 ES6 구문으로 React.Component를 상속받아 클래스 내부에 render() 메서드를 구현함으로써 사용자 인터페이스를 정의한다.
    
    ```jsx
    import { Component } from 'react';
    
    class Greeting extends Component {
      render() {
        return <h1>Hello, {this.props.name}!</h1>;
      }
    }
    ```
    
- 리액트가 순수 함수로 구현된 render() 메서드를 호출해 화면에 무엇을 표시해야 할 지를 결정한다.
    - [https://react.dev/reference/react/Component#render](https://react.dev/reference/react/Component#render)
- 부모 컴포넌트로부터 프로퍼티 properties 를 통해 정보를 받을 수 있다.
    - [https://react.dev/reference/react/Component#props](https://react.dev/reference/react/Component#props)

# 2.3 리액트 프래그먼트

- [https://react.dev/reference/react/Fragment](https://react.dev/reference/react/Fragment)
- React.Fragement 또는 <> … </>을 사용함으로써 다수의 엘리먼트를 그룹지을 수 있다.
- 그룹지어진 엘리먼트들은 단일 엘리먼트가 있어야할 곳에 사용가능하다.
- 프래그먼트를 사용해 엘리먼트를 그룹지어도 레이아웃이나 스타일에 아무 영향이 없기 때문에 다른 엘리먼트를 사용해서 감싸는 것에 비해 유용하게 사용할 수 있다.
    
    ```jsx
    function Post() {
      return (
        <>
          <PostTitle />
          <PostBody />
        </>
      );
    }
    ```