---
layout: post
title:  JS Array 객체
date:   2020-05-15 21:03:36 +0530
categories: Javascript
---
Array() 객체

Array 객체 사용
---
```javascript
let fruits = new Array('사과', '바나나')

console.log(fruits.length) // 2
console.log(fruits[0])     // "사과"

```

Array 메소드
---

```javascript
var arr = [ 1, 2, 3, 4 ];
arr.pop(); // 마지막인덱스를 반환하고 삭제
console.log( arr ); // [ 1, 2, 3 ]

var arr = [ 1, 2, 3, 4 ];
arr.push( 5 ); 
console.log( arr ); // [ 1, 2, 3, 4, 5 ]

//join은 배열 원소 전부를 하나의 문자열로 합친다.
var arr =[ 1, 2, 3, 4 ];
console.log( arr.join() );      // 1,2,3,4
console.log( arr.join( '-' ) ); // 1-2-3-4
```
pop, push, join 이 외의 메소드들이 많이 있다.

[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
