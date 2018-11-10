

###[What is domain logic?](https://enterprisecraftsmanship.com/2016/08/25/what-is-domain-logic/)  
When working on a project, you can point out two distinct areas: **problem space** and **solution space**.
>프로젝트를 진행할때 문제영역과 해결영역으로 나눌수있다.  
>problem space : 소프트웨어가 해결해야할 실제 문제  
>solution space : 문제 영역에 대한 솔루션


To do that, you need to look at **whether or not the code makes decisions that have a business meaning.** That is what differentiates domain logic. Your domain model is responsible for generating business-critical decisions while all other parts of your code base just interpret those decisions or provide input needed to make them.
>비즈니스 의미를 가지는 로직은 도메인로직으로 볼수있다.


None of the two code samples make the decision by themselves, they both delegate it to the domain model. That’s essentially how a proper separation of concerns often looks like. While the application services layer can contain quite a lot of code, **none of it should be about making any business-critical decisions. The only place for taking them is the domain model.**
>비즈니스 의사결정은 오직 도메인로직에 있어야 한다.

####Summary
Domain logic (aka business logic, business rules, and domain knowledge)  

All other types of logic orchestrate the decisions made by the domain model and transform them into side-effects: save them to the data store, show to the user, or pass to 3rd-party services.  
>도메인외 다른로직들은 도메인이 결정내린 사항을 저장하거나 전송하거나 다른 서비스로 요청을 보내는 것  

It’s important to separate domain logic from other types of logic as it helps keep the overall code base simpler.



---


###[Domain-Driven Design – What is it and how do you use it?](https://airbrake.io/blog/software-design/domain-driven-design)

Factories: As we’ve discussed through a number of design patterns articles already, DDD suggests the use of a factory, which encapsulates the logic of creating complex objects and aggregates, ensuring that the client has no knowledge of the inner-workings of object manipulation.
> factory 패턴으로 DDD root를 만들어 낸다는거 같은데 어떤케이스에서 쓰느거지... 예제가 필요해..

Domain Event: An object that is used to record a discrete event related to model activity within the system. While all events within the system could be tracked, a domain event is only created for event types which the domain experts care about.

> 모델상태변화에 따른 시스템에 발생시키는 이벤트 같은데 아직 잘..

#?
DDD Factories use case  
DDD Domain Event use case  


















