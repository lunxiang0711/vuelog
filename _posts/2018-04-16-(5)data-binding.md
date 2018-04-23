---
layout: post
date: 2018-04-16 13:00 
title: ................(3) 데이터 바인딩 및 전달 
comments: true
external-url:
categories: (02)nuxt.js
---

<br/>
### (3) 데이터 바인딩 및 전달 
-----
_데이터 바인딩하기_
<br/>

재사용 가능한 컴포넌트를 작성하기 위해서는 컴포넌트 내부에 하드코딩된 데이터를 변수로 대체하고 v-bind 태그를 이용해 바인딩해주어야 하며, props 프로퍼티를 이용해 바인딩되는 변수명을 지정해주어야 합니다.

```
변경되는 부분 : components/Recipe.vue
```

상세한 내용은 다음의 링크 [components/Recipe.vue](https://github.com/lunxiang0711/nuxt-recipes/commit/0f7537503dd07114b55003420e2d28f7f350a362)를 참고하시기 바랍니다.

-----
_데이터 전달하기_
<br/>

이제 컴포넌트에 데이터를 전달할 준비가 되었습니다. 컴포넌트 태그에 속성값을 지정하는 방식(props 프로퍼티를 이용해 미리 지정해둔 변수명을 사용)으로 데이터를 전달하는 일만 남았습니다.

```
변경되는 부분 : pages/recipes/index.vue
```
상세한 내용은 다음의 링크 [pages/recipes/index.vue](https://github.com/lunxiang0711/nuxt-recipes/commit/ec90ab2eb0e0f9479591813c46cd4646da1056fa)를 참고하시기 바랍니다.

-----
_나머지 컨텐츠에도 컴퍼넌트를 적용하기_

재사용 가능한 컴포넌트 작성이 완료되었으므로, 나머지 컨텐츠에도 동일한 컴포넌트를 같은 방식으로 적용하면 됩니다.

```
변경되는 부분 : pages/recipes/index.vue
```

상세한 내용은 다음의 링크 [pages/recipes/index.vue](https://github.com/lunxiang0711/nuxt-recipes/commit/64375084389c41c1aef130403c751566850386d5)를 참고하시기 바랍니다.


-----
_사용하지 않는 코드 정리_
<br/>

기존 템플릿 페이지에서 컨텐츠가 치환되었기 때문에, 사용하지 않는 스타일을 삭제해 줍니다.

```
변경되는 부분 : pages/recipes/index.vue
```

상세한 내용은 다음의 링크 [pages/recipes/index.vue](https://github.com/lunxiang0711/nuxt-recipes/commit/5cfd848d231aa3d26dd29a4d99d8e9fe6b0d9434)를 참고하시기 바랍니다.

-----

이것으로 part 1의 작성이 완료되었습니다. 간략히 요약하자면 part1에서는 페이지를 구성하는 방식과 컴포넌트가 작성하는 방식, 하드코딩된 코드를 컴포넌트로 치환하는 방식 등을 학습했습니다.
