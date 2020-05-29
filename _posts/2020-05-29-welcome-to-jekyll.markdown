---
layout: post
title:  "vue.js 기본 라우터 사용법"
date:   2020-05-29 21:03:36 +0530
categories: Vue.js
---

Vue.js의 기초

router
---

```javascript
routes: [
    {
      path: '/',
      name: 'Read',
      component: Read
    },
    {
      //동적세그먼트는 클론: 으로 표시 그래서 $route.params.contentId로 표시됨.
      path:'/create/:contentId?', //?가 붙은 이유는 contentId가 없어도 Create가 열려야하기 때문이다.
      name:'Create',
      component: Create //Create의 컴포넌트를 보여줄 것이다.
    },
    {
      path:'/detail/:contentId',
      name:'Detail',
      component: Detail //Create의 컴포넌트를 보여줄 것이다.
    },
  ]
```

router의 name과 path의 차이
---
```javascript
<button @click="home">처음으로</button> //프로그래밍 방식.

home(){
            this.$router.push({
                path:'/'
            })
        },

<router-link :to="{ name: 'Read'}">home</router-link> 
<!--//<router-link>를 사용하여 선언적 네비게이션용 anchor 태그를 만드는 것 -->
```



[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
