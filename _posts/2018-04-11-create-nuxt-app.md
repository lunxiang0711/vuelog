---
layout: post
date: 2018-04-11 13:00 
title: create-nuxt-app 
comments: true
external-url:
categories: (02)nuxt.js
---

> Nuxt.js는 Vue.js 애플리케이션을 보다 손쉽게 작성하고 배포할 수 있도록 돕는 프레임워크이며,
서버 사이드 렌더링(Server Side Rendering)을 이용하여 검색 엔진 최적화와 초기 로딩 속도를 개선하는 데 이용할 수도 있습니다.


Nuxt.js에 입문하기 전에 [Vue.js 공식 가이드 문서](https://kr.vuejs.org/v2/guide/index.html)를 통해 뷰 프레임워크의 기본 철학과 뷰 인스턴스
생성 방법, 템플릿 문법, 컴포넌트 등록 방법 등을 먼저 익히는 것이 좋습니다.

Nuxt 기본적인 폴더 구조(pages, layouts, components)와 관련한 렌더링 작동 방식, 라우팅 사용법
등을 소개하는 Youtube 동영상 튜터리얼 [Nuxt.js - Introduction by Project](https://www.youtube.com/watch?v=nteDXuqBfn0&t=618s)의 내용을 기초로 작성
 되었습니다.  

상기 튜터리얼은 [nuxt-community/create-nuxt-app](https://github.com/nuxt-community/starter-template)의 create-nuxt-app (cli 기반 템플릿 생성기)을
이용해 간단한 static website(갤러리 게시판)를 구현합니다. 
Nuxt.js 라이브러리 외에 webpack과 같은 bundler나 Bootstrap과 같은 UI framework을 사용하지 않아 작성하는 코드와 설명이 간결하고 깔끔한 것이 장점입니다.

본 문서에는 해당 동영상을 효과적으로 학습하는 데 도움을 주기 위한 code snippet, Github Compare View, 부연 설명 등이 포함될 예정입니다.

학습을 마친 이후에 vue와 webpack을 함께 사용하는 vue-cli(마찬가지로 cli 기반 템플릿 생성기)의
[vuejs-templates/webpack](https://github.com/vuejs-templates/webpack) 템플릿을 사용해보고 장단점을 비교해가는 것도 좋을 것 같습니다.



