---
layout: post
title:  "Node.js 기초"
date:   2020-05-21 21:03:36 +0530
categories: NodeJS
---

Node.js에 대한 이론

nodeJs란?
---
확장성 있는 네트워크 애플리케이션 개발에 사용되는 소프트웨어 플랫폼이다.
Non-blocking I/O와 단일 스레드 이벤트 루프를 통한 높은 처리 성능을 가지고 있다. 

Node.js와 관련된 핵심키워드 
---
- 구글 V8 자바스크립트 엔진
- 고성능 네트워크 서버
- 단일 쓰레드(Single Thread) 이벤트 루프(Event Loop) 기반
- 비동기 I/O 처리(Non-Blocking I/O)
- 자바스크립트
- 개발 생산성 향상
- 방대한 모듈 제공(NPM) 

쓰레드 기반 동기방식(Blocking I/O)
---
- 하나의 쓰레드가 request를 받으면 모든 처리가 완료될때까지 기다리다가 처리결과가 완료되면 다시 응답을 보냄
기존 업무 처리가 완료되기 전에 또다른 request가 있으면 새로운 쓰레드가 업무를 처리함.
동시 request가 많은 경우 많은 쓰레드가 필요하게 되어 서버 과부하

단일쓰레드 이벤트 루프 기반 비동기방식( Non-Blocking I/O)
---
하나의 쓰레드가 request를 받으면 바로 다음 처리에 요청을 보내놓고 다른 작업을 처리하다가 
먼저 요청한 작업이 끝나면 이벤트를 받아서 응답을 보낸다.
동시 request가 오더라도 처리가 완료될때까지 기다리지 않아도 되기 때문에 서버 부하가 적다.

Node.js로 서버 실행
---
```javascript
var http = require('http');
var fs = require('fs');
var app = http.createServer(function(request,response){
    var url = request.url;
    if(request.url == '/'){
      url = '/index.html';
    }
    if(request.url == '/favicon.ico'){
      return response.writeHead(404);
    }
    response.writeHead(200);
    response.end(fs.readFileSync(__dirname + url));
 
});
app.listen(3000);
```

[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
