---
layout: post
date: 2018-04-23 11:00 
title: 3...part 2 - (1) 뷰 라우팅 테스트
comments: true
external-url:
categories: (02)nuxt.js
---

> 동영상의 두번째 파트에서는 nuxt의 뷰-라우팅(vue-routing) 기능을 이용하여 렌더링을 하는 방법과 동적으로 페이지 라우팅(asyncData 메소드를 이용하여 서버와 비동기 통신을 수행하고, 이 과정에서 서버로부터 수신한 데이터를 이용하여 동적 라우팅 주소 생성)을 하는 방법을 다루고 있습니다.

<br/>
### (1) 뷰 라우팅 테스트
-----
_연결할 페이지(Recipe 상세) 새로 만들기_
<br/>

vue-router를 이용한 페이지 라우팅 사용 방법을 익히기 위해 추후에 Recipe 컴포넌트와 연결시킬 Recipe 상세 페이지를 작성합니다. 먼저 pages/recipes 폴더 아래에 _id 폴더를 만든 다음, 해당 폴더 하위에 index.vue 파일을 새로 만들고 라우팅 파라미터($route.params.id)가 잘 전달되는지 확인하는 간단한 템플릿 코드를 작성합니다. 


```
추가하는 부분 : pages/recipes/_id/index.vue
```
상세한 내용은 다음의 링크 [components/Recipe.vue](https://github.com/lunxiang0711/nuxt-recipes/commit/cf5155915b4351a6a524e087c30e642a5e3ca927)를 참고하시기 바랍니다.

-----
_연결할 페이지(Recipe 상세) 꾸미기_
<br/>

간단한 동적 페이지 라우팅의 동작을 확인했으므로 동적 페이지 라우팅을 테스트하기 위한 사전 준비로 Recipe 상세 페이지의 구조 및 스타일을 변경합니다. 

```
변경되는 부분 : pages/recipes/_id/index.vue
```
상세한 내용은 다음의 링크 [pages/recipes/_id/index.vue](https://github.com/lunxiang0711/nuxt-recipes/commit/a7edd5693fde9e9c71ab46f9e70d8278878f7001)를 참고하시기 바랍니다.

-----
_Recipe 컴포넌트와 Recipe 상세 페이지 연결_

Recipe 컴포넌트를 마우스로 클릭하면 Recipe 상세 페이지로 연결되도록 기존에 작성한 Recipe 컴포넌트의 템플릿의 root element를 nuxt-link 태그로 감싸주고 id 값이 전달될 수 있도록 props에 id 변수를 등록합니다.

```
변경되는 부분 : components/Recipe.vue
```

상세한 내용은 다음의 링크 [components/Recipe.vue](https://github.com/lunxiang0711/nuxt-recipes/commit/95b3736cffe9396b2c675a4942a2d3ac69551626)를 참고하시기 바랍니다.


-----
_라우팅에 사용될 id값을 전달하기_
<br/>

앞서 props에 등록한 id 변수값이 컴포넌트에 잘 전달되는지를 테스트하기 위해, Recipe 태그의 속성값에 id 및 상수값을 지정하여 Recipe 컴포넌트에 전달합니다.

```
변경되는 부분 : pages/recipes/index.vue
```

상세한 내용은 다음의 링크 [pages/recipes/index.vue](https://github.com/lunxiang0711/nuxt-recipes/commit/0fb395b6c5012a5082f60c2c6f34e10d674995be)를 참고하시기 바랍니다.


-----
_nuxt-link 스타일링하기_
<br/>

nuxt-link 태그는 렌더링 과정에서 a 태그로 변환되므로, 해당 태그 부분을 스타일링 할 때에는 a 태그에 css를 적용합니다.

```
변경되는 부분 : components/Recipe.vue
```

상세한 내용은 다음의 링크 [components/Recipe.vue](https://github.com/lunxiang0711/nuxt-recipes/commit/0a8c7a7aefa20942e1efb8868dfd37b55bced4d0)를 참고하시기 바랍니다.

-----

이것으로 part 2
