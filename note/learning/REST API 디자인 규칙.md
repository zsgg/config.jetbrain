![alt book](http://image.yes24.com/momo/TopCate251/MidCate007/25061723.jpg)

###여전히 우리는 다음과 같은 질문들에 대한 답을 찾아야 한다.
- URI 경로path 세그먼트는 언제 복수로 써야 하는가?  
- 리소스의 상태를 업데이트하려면, 어떤 메서드를 사용해야 하는가?  
- CRUD12가 아닌 연산을 어떻게 URL에 매핑하는가?  
- 특정한 시나리오에 가장 적합한 HTTP 응답은 무엇인가?  
- 리소스 상태 표현의 버전은 어떻게 관리할 수 있는가?  
- JSON에 포함된 하이퍼링크는 어떻게 구조화하는가?  

###리소스 모델링
http://api.soccer.restapi.org/leagues/seattle/teams/trebuchet  
이 URI 디자인은 다음과 같은 자체 리소스 주소를 가진 URI가 있다는 것을 뜻한다.  

- http://api.soccer.restapi.org/leagues/seattle/teams  
- http://api.soccer.restapi.org/leagues/seattle  
- http://api.soccer.restapi.org/leagues  
- http://api.soccer.restapi.org  

###리소스 원형
리소스 모델로 명확하고 정확하게 클라이언트와 통신하려면, REST API는 리소스 원형 중에서 리소스 하나로만 설계해야 한다.   
일관성을 위해 리소스 원형 하나 이상을 이용하여 리소스를 설계하지 않도록 주의를 기울여야 한다.  
대신, 링크를 통해 계층적으로 연관될 수 있는 분리된 리소스 설계를 고민해야 한다.

####도큐먼트
도큐먼트 리소스는 객체 인스턴스나 데이터베이스 레코드와 유사한 단일 개념이다.  
일반적으로 도큐먼트의 상태 표현은 값을 가진 필드와 다른 관련 리소스와의 링크 둘 다를 가지게 된다.  
기본적인 필드와 링크 기반 구조로 인해, 도큐먼트 타입은 다른 리소스 원형들의 기반 원형이 된다.  
즉, 서로 다른 리소스 원형 세 개는 도큐먼트 원형에서 분리된 것이라 볼 수 있다.  
다음 URI는 각각 도큐먼트 리소스를 나타낸다.  

- http://api.soccer.restapi.org/leagues/seattle  
- http://api.soccer.restapi.org/leagues/seattle/teams/trebuchet  
- http://api.soccer.restapi.org/leagues/seattle/teams/trebuchet/players/mike  

####컬렉션
컬렉션 리소스는 서버에서 관리하는 디렉터리라는 리소스다.

####스토어
스토어는 클라이언트에서 관리하는 리소스 저장소다.   
스토어 리소스는 API 클라이언트가 리소스를 넣거나 빼는 것, 지우는 것에 관여한다.

####컨트롤러
컨트롤러 리소스는 절차적인 개념을 모델화한 것이다.  
컨트롤러 리소스는 실행 가능한 함수와 같아서 파라미터(입력 값)와 반환 값(출력 값)이 있다.  
전통적인 웹 애플리케이션이 **'HTML form'을 사용하듯이, REST API는 CRUD라고 알려진 표준적인 메서드와는 논리적으로 매핑되지 않는 애플리케이션 고유의 행동을 컨트롤러 리소스의 도움을 받아 수행한다.**   
일반적으로 컨트롤러 이름은 URI 경로의 제일 마지막 부분에 표시되며, 계층적으로 뒤따르는 자식 리소스는 없다.   
다음 예제는 클라이언트가 사용자에게 경고를 재전송하게 하는 컨트롤러 리소스다.

####HTTP 요청 메서드 정리
GET 리소스의 상태를 일정한 표현 형태로 가져온다.  
HEAD 리소스의 메타데이터 상태를 가져온다.  
PUT 스토어에 새로운 리소스를 삽입하거나 기존 리소스를 갱신한다.  
DELETE 리소스를 부모 리소스에서 제거한다.  
OPTIONS 리소스의 가능한 상호작용을 기술하는 메타데이터를 가져온다.   
POST 오류(도큐먼트) | 새로운 리소스를 생성한다.(컬렉션) | 에러(스토어) | 함수를 실행한다.(컨트롤러)



###규칙

####규칙: 도큐먼트 이름으로는 단수 명사를 사용해야 한다
도큐먼트 리소스를 나타내는 URI는 단수 명사나 명사구를 포함하는 경로 부분으로 이름을 짓는다.  
예를 들면, 한 명의 선수 도큐먼트를 나타내는 URI는 단수 형태가 되어야 한다.

####규칙: 컬렉션 이름으로는 복수 명사를 사용해야 한다
컬렉션을 식별하는 URI는 복수 명사나 복수 명사구를 나타내는 명사로 경로의 이름을 지어야 한다.  
그리고 컬렉션 이름은 균일하게 포함되도록 선택해야 한다.

####규칙: 스토어 이름으로는 복수 명사를 사용해야 한다
리소스 스토어를 나타내는 URI는 복수 명사, 복수 명사구로 표현해야 한다.  
음악 플레이리스트 스토어의 URI는 다음과 같은 복수 명사 형태를 사용할 수 있다.  

- http://api.music.restapi.org/artists/mikemassedotcom/playlists

####규칙: 컨트롤러 이름으로는 동사나 동사구를 사용해야 한다
프로그램에 사용하는 함수처럼, 컨트롤 리소스를 나타내는 URI는 동작을 포함하는 이름으로 지어야 한다. 예를 들면 다음과 같이 짓는다.  

- http://api.college.restapi.org/students/morgan/register  
- http://api.example.restapi.org/lists/4324/dedupe  
- http://api.ognom.restapi.org/dbs/reindex  
- http://api.build.restapi.org/qa/nightly/runTestSuite  

####규칙: 경로 부분 중 변하는 부분은 유일한 값으로 대체한다
- http://api.soccer.restapi.org/leagues/{leagueId}/teams/{teamId}/players/{playerId}

####규칙: CRUD 기능을 나타내는 것은 URI에 사용하지 않는다
URI는 리소스를 식별하는 데만 사용해야 함

####URI Query 디자인
URI 구성요소인 쿼리는 유일한 리소스를 식별하는 데 도움을 준다. 다음 예를 보자. 
 
- http://api.college.restapi.org/students/morgan/send-sms ➊  
- http://api.college.restapi.org/students/morgan/send-sms?text=hello ➋  

리소스 URI 전체는 HTTP 캐시와 같은 네트워크 기반의 중개자에게 아무런 의미도 없어야 한다(쿼리 자체도 캐시 가능해야 한다는 의미다).  
URI의 쿼리 유무에 따라 캐시의 작용이나 기능이 바뀌어서는 안 된다.  
특히 요청 URI에 쿼리가 있다고 해서 응답 메시지가 캐시에서 제외되어서는 안 된다.


####규칙: URI 쿼리 부분으로 컬렉션이나 스토어를 필터링할 수 있다
URI 쿼리는 컬렉션이나 스토어의 검색 기준으로 사용하기에 적합하다. 다음 예를보자.  

- GET /users ➊   
- GET /users?role=admin ➋  


####규칙: GET 메서드나 POST 메서드를 사용하여 다른 요청 메서드를 처리해서는 안 된다
터널링tunneling은 메시지의 원래 의도를 감추거나 잘못 표현하는 것, 프로토콜의 투명성을 훼손하는 것 등의 HTTP 오용을 의미한다.


####규칙: PUT 메서드는 리소스를 삽입하거나 저장된 리소스를 갱신하는 데 사용해야 한다
PUT 메서드는 클라이언트가 기술한 URI로 스토어에 새로운 리소스를 추가하는데 사용한다.  
이미 스토어에 저장된 리소스를 갱신하거나 다른 것으로 대체하는 데도 PUT 메서드를 사용한다. 


####규칙: PUT 메서드는 변경 가능한 리소스를 갱신하는 데 사용해야 한다
클라이언트는 PUT 요청 메서드를 사용해서 리소스를 변경한다.  
PUT 요청 메시지에는 원하는 형태로 변경된 메시지 바디를 포함할 수 있다.


####규칙: POST 메서드는 컬렉션에 새로운 리소스를 만드는 데 사용해야 한다
클라이언트는 POST 메서드를 사용해서 컬렉션 안에 새로운 리소스를 만든다.  
POST 요청 바디는 새로운 리소스를 위해 제안된 상태 표현을 포함하는데, 이것은 서버 소유의 컬렉션에 추가된다.



####규칙: POST 메서드는 컨트롤러를 실행하는 데 사용해야 한다
클라이언트는 POST 메서드를 사용해서 기능 지향적인 컨트롤러 리소스를 동작시킨다.  
POST 요청 메시지는 컨트롤러 리소스 기능의 입력 값을 헤더나 바디에 포함할 수 있다.

HTTP 표준에서는 POST 메서드에 의미상의 제한을 두지 않으며, 반복이나 부작용과 상관없이 어떤 액션도 수행할 수 있다.  
이런 특징 때문에, POST 메서드를 제한 없는 컨트롤러 리소스로 사용할 수 있다.

####규칙: DELETE 메서드는 그 부모에서 리소스를 삭제하는 데 사용해야 한다
클라이언트는 DELETE 메서드 요청을 사용하여 컬렉션이나 스토어인 부모에서 리소스를 완전히 제거한다

####규칙: 진입 API URI 수를 최소화하라
REST API 설계 관점에서 웹을 보면, 홈페이지와 그와 연관된 웹 사이트 내비게이션이 도처에 있음을 고려해야 한다.  
API Docroot의 URI에서 사람이 읽을 수 있는 형태의 문서를 제공하는 것이 곧 REST API다.  
그 Docroot의 표현은 다른 모든 리소스를 프로그램적으로 사용할 수 있게 하는 링크를 제공해줘야 한다.  
서비스의 개별 리소스 URI나 URI 템플릿을 알려주는 API 문서는 클라이언트 개발자가 API URL을 불분명한 식별자로 취급하지 않게 하는 경향이 있다.  
대신 클라이언트 개발자는 API 하이퍼미디어를 이용해야 한다.





##ETC
####[https://stackoverflow.com/questions/18078210/where-to-store-resources-uris-in-a-rest-api](https://stackoverflow.com/questions/18078210/where-to-store-resources-uris-in-a-rest-api)
Do not store the URI in your database.  
The URI of a resource is not the resource itself. Also, you don't need to return the ID in your response. Clients have no need for it. Just return the URL for self and the URLs of any linked resources.

####[REST API: Put vs Post](http://1ambda.github.io/javascripts/rest-api-put-vs-post/)
(1) POST to a URL **creates a child resouce** at a server defiend URL  
(2) PUT to a URL **create/replaces the resource** in is entirely at the client defined URL  
(3) PATCH to a URL **updates part of the resource** at that client defined URL  


####[REST API: Put vs Post](https://1ambda.github.io/javascripts/rest-api-put-vs-post/)




###가이드
####[Google](https://cloud.google.com/apis/design/)
####[REST API 디자인 가이드](http://bcho.tistory.com/914)
####[(번역) RESTful API Designing guidelines — The best practices](https://wayhome25.github.io/etc/2017/11/26/restful-api-designing-guidelines/)
####[REST API 디자인 개요](https://www.slideshare.net/nexusz99/rest-api-48600643)
####[RESTful API를 설계하기 위한 디자인 팁](https://spoqa.github.io/2013/06/11/more-restful-interface.html)
####[REST](https://slides.com/eungjun/rest#/)




###리뷰
초반에 많은 도움이 됬다.   
특히 룰에 대한 설명이 자세히 나와있어서 처음 restful Api를 설계한다면 좋은 가이드 북이 될것이다.  
restful api는 표준이 없다 메이저 기업마다 자기만의 가이드를 가지고 있고 환경에 따라 달라지기도 한다. 이 책의 규칙에 대해서는 지키되 나의 api가이드를 만들어 봐야겠다.

**GraphQL**이라는게 rest를 대체할수도 있다한다. 알아보자

####store는 아직 뭔지 잘 모르겠다.