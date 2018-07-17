![alt book](http://image.yes24.com/momo/TopCate71/MidCate02/7017718.jpg)



####POST
몸체(Message Body) 또는 짐(Payload)에 파라미터를 보냄

####컨테이너
누군가는 Http Request Response를 만들어 줘야하는데 그게 컨테이너임

####Response 객체 쓰기작업을 한뒤에는 sendReedirect를 할수 없음

####ServletContext vs ServletConfig | p193
Jsp도 자기의 ServletConfig를 가짐

#####[ServletConfig와 ServletContext 의 차이점](http://oya150.tistory.com/entry/JSPServletConfig%EC%99%80-ServletContext-%EC%9D%98-%EC%B0%A8%EC%9D%B4%EC%A0%90)



####ServletContextListener
리스너 종류 다양함
HttpSessionAttributeListener : 세션에 속성이 추가 제거 수정되는 이벤트 들음
 - 세션 그 자체에 대한 리스너이기 때문에 DD에 정의 해줘야함
HttpSessionBindingListener : 속성에 자기가 추가되었는지 들음  
 - 속성이 세션에 추가될때 속성의 정보를 디비에 읽어온다든지 제거될때 디비를 업데이트 한다든질할때 사용
 - 세션속성(객체)에 대한 리스너이기 때문에 DD추가없음


####세가지 생존범위 : Context, Request, Session

####컨테이너는 클라이언트를 어떻게 구분하는가?
HTTP 프로토콜은 무상태 연결.
지속적인 연결이 아니기때문에 클라이언트가 맺는 두번째 요청이 똑같은 클라이언트인지 컨테이너는 모름

####클라이언트는 유일한 세션 ID가 필요하다
클라이언트가 제일 처음 요청을 보낼 때, 컨테이너는 클라이엉ㄴ트의 유일한 세션 ID를 생성함. 그리고 Response에[ 넣어서 클라이언트로 돌려보냄. 그다음부터 클라이언트가 요청을 보낼때는 이세션 ID를 함께 보냄

####쿠키는 세션을 사용하기 위해서만 필요하나요? 아니면 다른데서도 쓰나요?
원래 쿠키는 세션을 지원하기 위해서 고안된것이기는 하지만 다른데서도 씀




















