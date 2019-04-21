![alt book](https://t1.daumcdn.net/cfile/tistory/2719C34052EC1C3C11?original)

#종류
![alt book](https://t1.daumcdn.net/cfile/tistory/99365F365B6A155511)

###생성패턴

- Abstract Factory (추상 팩토리)   
> 동일한 주제의 다른 팩토리를 묶어 준다.
> Abstract factory pattern은 Strategy 와 Factory의 콜라보. 전략적인 공장이다.
> factory pattern의 상위호환이 아니다.

- Builder 
> 생성(construction)과 표기(representation)를 분리해 복잡한 객체를 생성한다
> 다른 의미의 Builder는 set 메서드를 노출하지 않으면서 유연한 인스턴스 생성을 위해 사용한다. 


- Factory Method 
> 생성할 객체의 클래스를 국한하지 않고 객체를 생성한다.
> 객체를 만들어내는 부분을 서브 클래스(Sub-Class)에 위임하는 패턴.
> 바뀔 수 있는 부분을 찾아내서 바뀌지 않는 부분하고 분리시켜야 한다는 원칙.

- Prototype (원형) 
> 기존 객체를 복제함으로써 객체를 생성한다.

- Singleton (단일체) 
> 한 클래스에 한 객체만 존재하도록 제한한다.


###구조패턴

- Adapter (적응자) 
> 인터페이스가 호환되지 않는 클래스들을 함께 이용할 수 있도록, 타 클래스의 인터페이스를 기존 인터페이스에 덧씌운다.

- Bridge (가교) 
> 추상화와 구현을 분리해 둘을 각각 따로 발전시킬 수 있다.

- Composite (복합체) 
>  0개, 1개 혹은 그 이상의 객체를 묶어 하나의 객체로 이용할 수 있다.

- Decorator (장식자) 
> 기존 객체의 매서드에 새로운 행동을 추가하거나 오버라이드 할 수 있다.

- Façade (퍼사드) 
> 많은 분량의 코드에 접근할 수 있는 단순한 인터페이스를 제공한다.

- Flyweight (플라이급) 
> 다수의 유사한 객체를 생성·조작하는 비용을 절감할 수 있다.

- Proxy (프록시) 
> 접근 조절, 비용 절감, 복잡도 감소를 위해 접근이 힘든 객체에 대한 대역을 제공한다.


###행위패턴

- Chain of Responsibility (책임연쇄) 
> 책임들이 연결되어 있어 내가 책임을 못 질 것 같으면 다음 책임자에게 자동으로 넘어가는 구조

- Command (명령) 
> 위의 명령어를 각각 구현하는 것보다는 위 그림처럼 하나의 추상 클래스에 메서드를 하나 만들고 각 명령이 들어오면 그에 맞는 서브 클래스가 선택되어 실행하는 것

- Interpreter (해석자) 
> 문법 규칙을 클래스화한 구조를 갖는SQL 언어나 통신 프로토콜 같은 것을 개발할 때 사용

- Iterator (반복자) 
> 반복이 필요한 자료구조를 모두 동일한 인터페이스를 통해 접근할 수 있도록 메서드를 이용해 자료구조를 활용할 수 있도록 해준다.

- Mediator (중재자) 
> 클래스간의 복잡한 상호작용을 캡슐화하여 한 클래스에 위임해서 처리 하는 디자인 패턴

- Memento (메멘토) 
> Ctrl + z 와 같은 undo 기능 개발할 때 유용한 디자인패턴. 클래스 설계 관점에서 객체의 정보를 저장

- Observer (감시자) 
> 어떤 클래스에 변화가 일어났을 때, 이를 감지하여 다른 클래스에 통보해주는 것

- State (상태) 
> 동일한 동작을 객체의 상태에 따라 다르게 처리해야 할 때 사용하는 디자인 패턴

- Strategy (전략) 
> 알고리즘 군을 정의하고 각각 하나의 클래스로 캡슐화한 다음, 필요할 때 서로 교환해서 사용할 수 있게 해준다.

- Template Method 
> 상위 클래스에서는 추상적으로 표현하고 그 구체적인 내용은 하위 클래스에서 결정되는 디자인 패턴

- Visitor (방문자) 
> 각 클래스의 데이터 구조로부터 처리 기능을 분리하여 별도의 visitor 클래스로 만들어놓고 해당 클래스의 메서드가 각 클래스를 돌아다니며 특정 작업을 수행하도록 하는 것

---

component pattern ?

---

#ref
###[design-patterns-JS](https://github.com/fbeline/design-patterns-JS)
###[Design Patterns in Java Tutorial](https://www.tutorialspoint.com/design_pattern/index.htm)
###[JDM's Blog](https://jdm.kr/blog/)

---

#[Abstract Factory](https://ko.wikipedia.org/wiki/%EC%B6%94%EC%83%81_%ED%8C%A9%ED%86%A0%EB%A6%AC_%ED%8C%A8%ED%84%B4)
![image](https://upload.wikimedia.org/wikipedia/commons/9/9d/Abstract_factory_UML.svg)  
추상 팩토리 패턴(Abstract factory pattern)은 다양한 구성 요소 별로 '객체의 집합'을 생성해야 할 때 유용하다. 이 패턴을 사용하여 상황에 알맞은 객체를 생성할 수 있다. 
###[java abstract factory pattern (추상 팩토리 패턴)](https://blog.seotory.com/post/2016/08/java-abstract-factory-pattern)
###[자바 디자인패턴(Java Design Pattern)](http://oniondev.egloos.com/9663271)
###[추상 팩토리 패턴 Abstract Factory Pattern](https://dev-momo.tistory.com/entry/%EC%B6%94%EC%83%81-%ED%8C%A9%ED%86%A0%EB%A6%AC-%ED%8C%A8%ED%84%B4-Abstract-Factory-Pattern)
###[추상 팩토리 패턴이란](https://gmlwjd9405.github.io/2018/08/08/abstract-factory-pattern.html)

#[Factory Method](https://ko.wikipedia.org/wiki/%ED%8C%A9%ED%86%A0%EB%A6%AC_%EB%A9%94%EC%84%9C%EB%93%9C_%ED%8C%A8%ED%84%B4)
###[팩토리 메소드 패턴(Factory Method Pattern)](https://jdm.kr/blog/180)
###[java factory pattern (팩토리 패턴)](https://blog.seotory.com/post/2016/08/java-factory-pattern)


#[Builder](https://ko.wikipedia.org/wiki/%EB%B9%8C%EB%8D%94_%ED%8C%A8%ED%84%B4)
###[빌더 패턴(Builder Pattern)](https://johngrib.github.io/wiki/builder-pattern/)
###[Java 8 lambdas and the builder pattern](https://leelevett.wordpress.com/2014/06/27/java-8-lambdas-and-the-builder-pattern/)
###[++ Builder 패턴 정리](https://javaplant.tistory.com/22)


#[Prototype](https://ko.wikipedia.org/wiki/%ED%94%84%EB%A1%9C%ED%86%A0%ED%83%80%EC%9E%85_%ED%8C%A8%ED%84%B4)
###[java prototype pattern (프로토타입 패턴)](https://blog.seotory.com/post/2015/09/java-prototype-pattern)
우리가 db로 부터 데이터를 가져온 경우를 생각해보자. 프로그램 내에서 여러번 데이터 수정이 이루어진다고 할 때, 똑같은 데이터를 매번 db에서 가져오는 것은 좋은 생각은 아니다. prototype pattern은 이런 문제점을 해결하기 위해 원래의 object의 property들을 확인하여 deep 또는 shallow copy(얕은 카피, 깊은 카피)를 시도하여 clone object를 제공해준다.

###[Design Patterns - Prototype Pattern](https://www.tutorialspoint.com/design_pattern/prototype_pattern.htm)
prototype 패턴과 factory 또는 abstract factory와 같이 사용할수도 있다.

#[Singleton](https://ko.wikipedia.org/wiki/%EC%8B%B1%EA%B8%80%ED%84%B4_%ED%8C%A8%ED%84%B4)
###[Multi Thread 환경에서의 올바른 Singleton](https://medium.com/@joongwon/multi-thread-%ED%99%98%EA%B2%BD%EC%97%90%EC%84%9C%EC%9D%98-%EC%98%AC%EB%B0%94%EB%A5%B8-singleton-578d9511fd42)


---


#[Adapter](https://ko.wikipedia.org/wiki/%EC%96%B4%EB%8C%91%ED%84%B0_%ED%8C%A8%ED%84%B4)
###[어댑터 패턴(Adapter Pattern)](https://jdm.kr/blog/11)
사용처에서 클래스의 변경으로 많은 수정이 필요해질때 adapter를 중간에 두고 아무일없던것 처럼 기존 코드 호환을 만족시켜줄 수 있음.

#[Bridge](https://ko.wikipedia.org/wiki/%EB%B8%8C%EB%A6%AC%EC%A7%80_%ED%8C%A8%ED%84%B4)
###[Bridge 패턴](https://simsimjae.tistory.com/226)
###[Bridge 패턴](https://effectiveprogramming.tistory.com/entry/Bridge-%ED%8C%A8%ED%84%B4)
###[Bridge 패턴 (기능계층과 구현계층 분리하기)](https://m.blog.naver.com/PostView.nhn?blogId=tradlinx0522&logNo=220928963011&proxyReferer=https%3A%2F%2Fwww.google.com%2F)
기능계층과 구현계층의 분리를 통해 코드를 분리함  
기능(동물-공격), 구현(공격 방법)  
기능(게임유저-공격), 구현(들고 있는 무기의 공격방법)  
두 구체 클래스 간의 강한 결합을 제거하기 위해서 사용하는 패턴  


#[Composite](https://ko.wikipedia.org/wiki/%EC%BB%B4%ED%8F%AC%EC%A7%80%ED%8A%B8_%ED%8C%A8%ED%84%B4)
![image](https://upload.wikimedia.org/wikipedia/commons/5/5a/Composite_UML_class_diagram_%28fixed%29.svg)
컴포지트 패턴(Composite pattern)이란 객체들의 관계를 트리 구조로 구성하여 부분-전체 계층을 표현하는 패턴으로, 사용자가 단일 객체와 복합 객체 모두 동일하게 다루도록 한다.  



#[Decorator](https://ko.wikipedia.org/wiki/%EB%8D%B0%EC%BD%94%EB%A0%88%EC%9D%B4%ED%84%B0_%ED%8C%A8%ED%84%B4)
![image](https://upload.wikimedia.org/wikipedia/commons/e/e9/Decorator_UML_class_diagram.svg)  
데코레이터 패턴(Decorator pattern)이란 주어진 상황 및 용도에 따라 어떤 객체에 책임을 덧붙이는 패턴으로, 기능 확장이 필요할 때 서브클래싱 대신 쓸 수 있는 유연한 대안이 될 수 있다.   

###[[Design Pattern] 데코레이터 패턴이란](https://gmlwjd9405.github.io/2018/07/09/decorator-pattern.html)
###[데코레이터 패턴(Decorator Pattern)](https://jdm.kr/blog/78)
클래스를 써서 기능을 확장하는 방법이고 프로그램을 실행하는 중에도 객체를 확장 시킬 수 있는 패턴
`BufferedReader br = new BufferedReader(new FileReader(new File("test.txt")));`

#[Proxy](https://ko.wikipedia.org/wiki/%ED%94%84%EB%A1%9D%EC%8B%9C_%ED%8C%A8%ED%84%B4)
![image](https://upload.wikimedia.org/wikipedia/commons/7/75/Proxy_pattern_diagram.svg)
  
###[프록시 패턴(Proxy Pattern)](https://jdm.kr/blog/235)
실제 기능을 수행하는 객체Real Object 대신 가상의 객체Proxy Object를 사용해 로직 흐름제어
가상 프록시(Virtual Proxy) 와 보호 프록시(Protection Proxy)가 있다.  















