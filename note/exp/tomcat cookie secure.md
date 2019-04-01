https에서 발행한 세션쿠키를 이용해 로그인을 처리하면
http 페이지에서 secure 속성이 true인 쿠키를 보내지못해 새로운 접속이라고 서버에서 판단하고 새로운 새션아이디를 생성해 보내준다.

만약 https 로그인 페이지에서 로그인 후 http 페이지로 location href 시킨다면 무한 핑퐁 현상이 발생됨..

해결하기 위해서는 session id를 가지는 쿠키의 속성값중 secure를 false로 변경해 줘야한다.

**특이사항**
크롬은 true되어도 핑퐁현상이 없는데 파폭은 거의 100% 발생함

###ref
[Http와 Https 프로토콜 간에 안전하게 세션 공유하기](https://reiphiel.tistory.com/entry/http-https-share-session-secure)  
[쿠키(Cookie) 그리고 세션(Session)](https://nesoy.github.io/articles/2017-03/Session-Cookie)
