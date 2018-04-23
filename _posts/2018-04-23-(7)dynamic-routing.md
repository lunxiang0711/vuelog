---
layout: post
date: 2018-04-23 13:00 
title: ................(2) 동적 라우팅 테스트
comments: true
external-url:
categories: (02)nuxt.js
---

<br/>
### (2) 동적 라우팅 테스트
-----
_라우팅 파라미터 추가_
<br/>

```
변경하는 부분 : pages/recipes/_id/index.vue
```

라우팅 파라미터를 연결할 페이지의 템플릿에 id값이 출력하도록 코드를 작성합니다.

상세한 내용은 다음의 링크 [components/Recipe.vue](https://github.com/lunxiang0711/nuxt-recipes/commit/08e8eaf97a8ea6585552d09785326cc1c45ce227)를 참고하시기 바랍니다.

-----
_Promise 메소드를 사용하여 비동기로 데이터 전달하기_
<br/>
```
변경하는 부분 : pages/recipes/index.vue
```

서버로부터 수신된 데이터를 통해 동적 페이지 라우팅이 생성되는 것처럼 시뮬레이팅하기 위해 Promise 메소드를 이용해 페이지 로딩 후 약 1.5초 후 recipes 객체가 전달되도록 스크립트를 작성한 뒤, Recipe 태그의 속성에 recipes 객체의 속성이 연결되도록 바인딩합니다.

상세한 내용은 다음의 링크 [pages/recipes/index.vue](https://github.com/lunxiang0711/nuxt-recipes/commit/a70f50f2153374bb24d35d864d70d0ef4046622b)를 참고하시기 바랍니다.

-----
_나머지 컴퍼넌트 태그에도 데이터 바인딩하기_
<br/>

나머지 id 2에 해당하는 코드 부분도 상기와 같이 바인딩 작업을 합니다.

```
변경되는 부분 : pages/recipes/index.vue
```
상세한 내용은 다음의 링크 [pages/recipes/index.vue](https://github.com/lunxiang0711/nuxt-recipes/commit/04543147776f4b7b6b20fb4ae29ff007350e9d6b)를 참고하시기 바랍니다.

-----
_v-for 디렉티브를 이용하여 반복코드 제거하기_
<br/>


반복적으로 나타나는 Recipe 태그 코드 부분을 v-for 디렉티브를 이용한 순환문으로 치환합니다.

```
변경되는 부분 : components/Recipe.vue
```

상세한 내용은 다음의 링크 [components/Recipe.vue](https://github.com/lunxiang0711/nuxt-recipes/commit/95b3736cffe9396b2c675a4942a2d3ac69551626)를 참고하시기 바랍니다.


-----
_Recipe 상세 페이지에 비동기 통신 데이터 전달하기_
<br/>

asyncData 메소드를 사용하되 recipe 배열 객체 반환시 filter를 적용하여 요청된 파라미터 id값과 일치하는 배열 요소만 반환하도록 코드를 작성합니다.

```
변경되는 부분 : pages/recipes/_id/index.vue
```

상세한 내용은 다음의 링크 [pages/recipes/_id/index.vue](https://github.com/lunxiang0711/nuxt-recipes/commit/f49ef63139b155ea463dd1d0cc55f1e0ee399b30)를 참고하시기 바랍니다.

