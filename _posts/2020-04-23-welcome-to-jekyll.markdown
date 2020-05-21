---
layout: post
title:  JS 함수 사용법
date:   2020-04-23 21:03:36 +0530
categories: Javascript NodeJS
---
화살표 함수

```javascript
function test1(f) {   
    let result = f(3, 4);   
    console.log(result); 
    } 

let add = (a, b) => {   
    return a + b; 
    } 

let multiply = (a, b) => {
    return a * b; 
    } 
test1(add); 
test1(multiply);

```
=(a,b) = > {} // 이부분이 파라미터 값으로 전달되는 함수이다.

익명 함수
---

```javascript
let f = function (msg) {   
    console.log(msg) 
    } 
f("hello")
//function (msg) {console.log(msg)} 이 부분이 익명함수 이다 
(function (msg) {   console.log(msg) })("hello")

```
Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk].

[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
