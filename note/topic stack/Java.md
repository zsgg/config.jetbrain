
###[Hashtable vs SynchronizedMap vs ConcurrentHashMap](https://codepumpkin.com/hashtable-vs-synchronizedmap-vs-concurrenthashmap/)
![alt book](https://codepumpkin.com/wp-content/uploads/2017/09/ConcurrentHashMap.jpg)
>**ConcurrentHashMap** divides the Map instance into different segments. And each thread acquires lock on each segment. By default it allows 16 threads to access it simultaneously without any external synchronization i.e. by default concurrency level is 16. We can also increase or decrease the default concurrency level while creating 

###[Java Volatile 의미](http://thswave.github.io/java/2015/03/08/java-volatile.html)
Java volatile 키워드는 여러개의 쓰래드들 에서 사용되는 변수의 변화(값의 변화) 에 대한 가시성의 보장합니다.


###[atomic vs volatile vs synchronized](http://mygumi.tistory.com/112)
>#####[What is the difference between atomic / volatile / synchronized?](https://stackoverflow.com/questions/9749746/what-is-the-difference-between-atomic-volatile-synchronized)


volatile의 경우는 하나의 스레드가 쓰기 연산을 하고, 다른 스레드에서는 읽기 연산을 통해 최신 값을 가져올 경우. 즉 다른 스레드에서는 업데이트를 행하지 않을 경우 이용할 수 있다.  
Atomic*** 클래스의 경우는 여러 스레드에서 읽기 쓰기 모두 이용할 수 있다. (CAS)  
synchronized 경우도 여러 스레드에서 읽기 쓰기 모두 이용할 수 있다. (Lock)  

---

###throws Throwable
![alt error tree](https://lh5.googleusercontent.com/WqqNoyFEkZXfmZBBQjgIutY72_BUV6_By_BAe7Ih9u36HfelS3nTWQEYtdRUkQS32Tuhg9P9CUXo-jgvOpkO84vLm2viI4Od0BNustwONdMm7DKZnKC6kyVHyRJbsESLIPV4uBU)
#####[자바의 예외처리](https://brunch.co.kr/@kd4/5)
Effective Java
>자바 언어 명세에 강제된 사항은 아니지만, 보통 Error는 JVM이 자원부족이나 프로그램을 실행할 수 엇는 상태에 도달했음을 알리기 위해 사용한다.  

>복구가능한 상태에서는 점검 지정예외(checked exception)를 사용하고, 프로그래밍 오류를 나타내고 싶을때는 실행지점 예외(runtime exception)를 사용하라는 것이다.

>unchecked나 error는 catch로 처리할 필요가 없으며, 일반적으로 처리해서도 안된다.  
프로그램이 무점검예외나 오류를 던진다는 것은 복구가 불가능한 상황에 직면했다는 뜻으로, 더 진행해 봐야 득보다 실이 더 크다는 뜻이다. 이런 throwable을 catch하지 않는 스레드는적절한 오류 메시지를 내면서 중단(halt)된다.



