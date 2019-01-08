![alt book](http://image.kyobobook.co.kr/images/book/large/162/l9791185885162.jpg)





#방법론
######[SMACSS, BEM, OOCSS - nts-corp](https://wit.nts-corp.com/2015/04/16/3538)
######[SMACSS, BEM, OOCSS - gomdoreepooh](https://gomdoreepooh.github.io/notes/smacss-bem-oocss)


#책에서 처음본 CSS(Cascading Style Sheets)
display:flow-root  
>자식이 float이 되어도 쪼그라드는걸 방지함  

shape-outside:circle(50%)
>float 속성이 있을때 적용되며. 이미지에 텍스트같은걸 두를때 사용

position:sticky
>위치가 상대적인것처럼 행동하다가 뷰포트가 top 위치에 도달할때 fixed 처럼 행동함

column-count:3 || column-width:200px
>요소를 단으로 나눔, 신문처럼

flex-wrap
>item이 부모영역을 벚어나지 않고 아래로 내려가게 만든다  

repeat(auto-fill, minmax(100px, 1fr)) || repeat(auto-fit, minmax(100px, 1fr))
>반응형 음음 꽉차게 만드는데 fill은 min따라가고 빈공간은 남겨둔다 fit은 반대

flex-basis
>flex의 너비나 높이

flex-grow
>0보다 크면 flex가 늘어날수 있다는것, 숫자는 비중을 의미함

flex-shrink
>0보다 크면 flex가 줄어들수 있다는것, 숫자는 비중을 의미함

flex
>flex-grow, shrink, basis 의 축약형



#리뷰

하루만에 책을 다 읽기는 처음인거 같다. (그 만큼 책이 그리 두껍지는 않음)
CSS와 나는 처음에는 악연 이였다가 이제 좋아지기 시작한다 그래도 IE는 싫음, 단호  

회사에서 IE 지원을 하다보니 안쓰는건 처음보는게 많고
처음보는걸 쓰려고 보면 지원하지않는다 그래서 의도적으로 처음보는 명세를 처다도 보지않게 되었다. 그러다가 구버전 지원안해도 되는 페이지를 개발하는 일이 생겼고 드디어! 나도 flex grid를 쓸수있다.  

구글링으로 검색해서 알음알음 알고 배운것들을 유용하게 썻지만 역시 검색에 드는 시간과 검색결과의 구성은 마음에 들지 않았다. 역시 책으로 보는것이 좋음.   

grid flex는 완벽하지는 않지만 효과적으로 쓸정도는 알수있게 되었다. 물론 책을 아주 아주 정독하지 않았기 때문이고 만약 각잡고 정독했다면 100%이지 않을까. 그 만큼 gird flex에 대해서는 자세하게 설명되어 있고 글이 많이있어 github의 코드와 함께 보는걸 추천한다.














