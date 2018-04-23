---
layout: post
date: 2018-04-16 12:00 
title: 3...part 1 - (1) 기본 페이지 작성하기
comments: true
external-url:
categories: (02)nuxt.js
---

> 본 문서 작성의 바탕이 되는 동영상 튜토리얼에서 작성하는 프로젝트는 크게 두 부분으로 구성되어 있습니다. 첫번째로 컴포넌트와 레이아웃을 이용하여 기본 페이지를 구성합니다. 두번째로 nuxt의 라우팅 기능을 이용하여 렌더링을 하는 방법을 다룹니다. 

<br/>
## part1 : nuxt의 기본 동작 이해하기 

### (1) 기본 페이지 작성하기

-----

cli를 이용하여 npm run dev 명령을 실행한 상태에서, 특정 URI에 대한 HTTP 요청이 잘 처리되는지를 확인하기 위해 아래와 같은 vue 파일을 먼저 작성합니다.

```
pages/about.vue

<template>
  <h1>THE ABOUT PAGE</h1>
</template>

```
<br/>
서버가 실행된 상태에서 vue 파일을 작성하면 자동으로 vue 파일이 렌더링 되고, 클라이언트 사이드 렌더링 작동 여부를 확인하기 위해 http://localhost:3000/about에 접속하면 아래와 같은 페이지가 나타나는 것을 확인할 수 있습니다.
<br/>

![](/assets/about.jpg)

<br/>

앞에서 확인 한 바와 같이 nuxt는 파일 이름을 기준으로 한 페이지 라우팅을 지원하며, 폴더 이름을 기준으로 페이지 라우팅을 할 수도 있습니다.

<br/>
따라서 about.vue 파일명을 index.vue로 변경한 뒤 pages/about 폴더 하위에 위치시켜도 동일한 렌더링 결과를 얻을 수 있습니다.
<br/>

```
업데이트 된 내용 : pages/about.vue → pages/about/index.vue
```
<br/>


다음으로는 pages 폴더 아래에 recipes/index.vue 파일을 만들고 아래와 깉이 실제 컨텐츠를 담을 페이지를 작성합니다.

```
새로 작성하는 내용 : recipes/index.vue

<template>
  <section class="recipes">
      <article class="recipe">
          <div class="thumbnail" 
               style="background-image: url('https://bit.ly/2GVYWM2')"></div>
          <h1>Title</h1>
          <p>Some nice preview text</p>
      </article>
      <article class="recipe">
          <div class="thumbnail"
               style="background-image: url('https://bit.ly/2qtNwou')"></div>
          <h1>Title</h1>
          <p>Some nice preview text</p>
      </article>
  </section>
</template>

<style scoped>

.recipes {
    display: flex;
    flex-flow: row wrap;
    justify-content: center;
    align-items: center;
}

.recipe {
    box-sizing: border-box;
    width: 280px;
    padding: 8px;
    border: 1px solid #ccc;
    box-shadow: 0 2px 2px #aaa;
    margin: 10px;
}

.thumbnail {
    background-position: center;
    background-size: cover;
    width: 100%;
    height: 200px;
}


</style> 

```
