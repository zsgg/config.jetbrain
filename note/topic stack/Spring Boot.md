

#Non-blocking & Asynchronous & Concurrency
###[멈추지 않고 기다리기(Non-blocking)와 비동기(Asynchronous) 그리고 동시성(Concurrency)](https://tech.peoplefund.co.kr/2017/08/02/non-blocking-asynchronous-concurrency.html)
>[[용어사전] Polling방식과 Interrupt방식](http://www.mcublog.co.kr/397)  




#[Spring WebFlux[번역 및 개인견해]](https://ztkmkoo.github.io/2017/12/13/spring-webflux/)


#Spring boot With DDD
###[Domain-Driven Design and Spring](http://static.olivergierke.de/lectures/ddd-and-spring/)
todo










#Functional Reactive Programming (FRP)
###[What is (functional) reactive programming?](https://stackoverflow.com/questions/1028250/what-is-functional-reactive-programming)
####[Reactive programming](https://en.wikipedia.org/wiki/Reactive_programming)  
>I've read the Wikipedia article on

todo


####[Functional reactive programming](https://en.wikipedia.org/wiki/Functional_reactive_programming)  
>I've also read the small article on

todo

####[What is Reactive Programming?](http://paulstovell.com/blog/reactive-programming)
>here's a guy with an active imagination and good storytelling skills take on the whole thing

todo

####[The introduction to Reactive Programming you've been missing](https://gist.github.com/staltz/868e7e9bc2a7b8c1f754)
>Another excellent FRP intro  
>One of the best i have seen, Example based  
>[번역: What is Reactive Programming?](https://medium.com/@Alpaca_iOSStudy/what-is-reactive-programming-669e4e804452)  
>[Reactive Programming 개요](http://wiki.sys4u.co.kr/pages/viewpage.action?pageId=8552930)  
todo
todo : reactive 원칙 4가지

###java8 Stream이란
todo

###Rx Java
todo

###[Reactive Programming과 Rx](https://m.blog.naver.com/jdub7138/220983291803)  
>"자료 처리를 수학적 함수의 계산으로 취급하고 상태와 가변 데이터를 멀리하는 프로그래밍 패러다임의 하나이다" - 출처 위키백과  

**개발자의 입장**   
비동기적 데이터 흐름으로 처리하는 프로그래밍 = Asynchronous Dataflow Programming  
모든것을 비동기적 데이터의 Stream으로 간주하고 Observer 디자인 패턴을 활용하여 이러한 비동기 이벤트를 처리  

**사용자의 입장**  
실시간으로 반응하는 프로그래밍, 예) 네이버 검색창에 단어를 하나씩 입력할 때마다 관련 검색어들이 자동완성으로 바로 바로 제시되는 것. 페이스북 포스트에 좋아요 **버튼을 누르면** 해당포스트를 보고 있는 다른 유저의 좋아요 카운트가 새로고침 없어도 실시간을 올라가는 것을 말함  

이는 명령형 프로그래밍(Imperative Programming)과 대비되는 개념, 예) 명령형은 a + b = c 일때 a b 가 바껴도 재연산을 하지않는 이상 c 는 변하지 않음 하지만 반응형은 b c 가 변할때 마다 바로바로 재연산이 수행되어 a가 실시간으로 변함  

####**Reactive Programming의 핵심은 Async와 Observer**   

CallBack으로 처리할수도 있지만 그러면 CallBack Hell이됨  


####**Functional Reactive Programming**  
Reactive Programming을 Functional Programming의 원리를 통해 구현하는 것을 말함.  

**Functional Programming 이란**  (static이 static 함)  
어떤 문제를 해결하는데 있어서 그 과정이나 공식에 매몰되기 보다는 그냥 이미 만들어진 함수를 활용하는 방식을 말함.  

다만, 무조건 활용하는 것이 아니라 함수 자체가 숨겨진 input output이 없도록 설계하는것이 전제조건.   

**Rx(ReactiveX)**  
비동기적인 이벤트를 손쉽게 처리하기 위해 만들어진 Api  
   
Rx에서는 모든것이 Data Stream이다.  

Rx에서는 Stream을 Obserable이라고 표현함. 그리고 해당 Obserable이 언제(When), 그리고 무엇을(What)분출하는지 듣고 있기 위해 Subscribe를 하게됨.  

###1급 함수에서 1급의 의미  
- 파라미터로 전달될 수 있다  
- 리턴 값으로 사용될 수 있다  
- 변수에 할당할 수 있다  
- 런타임에 생성될 수 있다  








#Spring Reactive Stack
###[WebFlux Reference Documentation](https://docs.spring.io/spring/docs/current/spring-framework-reference/web-reactive.html#spring-webflux)
todo

###[Notes on Reactive Programming Part I: The Reactive Landscape](https://spring.io/blog/2016/06/07/notes-on-reactive-programming-part-i-the-reactive-landscape#reactive-use-cases)
동시성과 병렬성이 필요한 프로그래밍에서 FRP(Functional Reactive Programming)은 효율이 좋다.

**Reactive Use Cases**

- External Service Calls
- Highly Concurrent Message Consumers
- Spreadsheets 
- Abstraction Over (A)synchronous Processing 

**Reactive Programming in Java**  
자바는 태생이 Reactive 하지 않지만 최근에 Reactive 레이어가 생기면서 몇가지를 살펴보고 사용하면 된다.

- [Reactive Streams](http://www.reactive-streams.org/)  
- [RxJava](https://github.com/ReactiveX/RxJava/wiki)  
- [Reactor](https://projectreactor.io/)
- [Spring Framework 5.](https://spring.io/projects/spring-framework)  
- [ratpack](https://ratpack.io/)
- [akka](https://akka.io/)

**Why Now?**  
상황, 해결해야하는 문제에 따라 Reactive는 훌륭한 포퍼먼스를 보여주고 문제를 해결해줄것이다 하지만, Reactive와 맞지않는 문제라면 상황이 악화될 수 있다.






####[Reactive Programming in the Netflix API with RxJava](https://medium.com/netflix-techblog/reactive-programming-in-the-netflix-api-with-rxjava-7811c3a1496a)




####[Reactive Streams](http://www.reactive-streams.org/)










###[Notes on Reactive Programming Part II: Writing Some Code](https://spring.io/blog/2016/06/13/notes-on-reactive-programming-part-ii-writing-some-code)






















