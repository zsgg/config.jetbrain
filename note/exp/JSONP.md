####[JSONP 알고 쓰자](http://kingbbode.tistory.com/26)
자바 스크립트는 서로 다른 도메인에 대한 요청을 보안상 제한합니다.  
이 정책을 동일근원정책(Same-Origin Policy, SOP) 정책이라고 하며, 이러한 정책으로 인해 생기는 이슈를 cross-domain 문제라고 합니다. 

script 요소는 src를 호출한 결과를 javascript를 불러와서 포함시키는 것이 아니고 실행시키는 태그입니다.

의 호출 후 즉시 실행하는 점을 이용하여 응답으로 온 Text Type의 결과를 javascript로 인식하여 바로 실행하게 됩니다.

```
var script = document.createElement('script');  
script.src = '//kingbbode.com/jsonp?callback=myCallback';  
document.getElementsByTagName('head')[0].appendChild(script);   
function myCallback(data){ //callback method }  
```

####[자바스크립트 예제로 살펴보는 JSONP의 기본원리](http://dev.epiloum.net/1311)

