###[Hashtable vs SynchronizedMap vs ConcurrentHashMap](https://codepumpkin.com/hashtable-vs-synchronizedmap-vs-concurrenthashmap/)
![alt book](https://codepumpkin.com/wp-content/uploads/2017/09/ConcurrentHashMap.jpg)
>**ConcurrentHashMap** divides the Map instance into different segments. And each thread acquires lock on each segment. By default it allows 16 threads to access it simultaneously without any external synchronization i.e. by default concurrency level is 16. We can also increase or decrease the default concurrency level while creating 

###[Java Volatile 의미](http://thswave.github.io/java/2015/03/08/java-volatile.html)
Java volatile 키워드는 여러개의 쓰래드들 에서 사용되는 변수의 변화(값의 변화) 에 대한 가시성의 보장합니다.


###[atomic vs volatile vs synchronized](http://mygumi.tistory.com/112)
volatile의 경우는 하나의 스레드가 쓰기 연산을 하고, 다른 스레드에서는 읽기 연산을 통해 최신 값을 가져올 경우. 즉 다른 스레드에서는 업데이트를 행하지 않을 경우 이용할 수 있다.  
Atomic*** 클래스의 경우는 여러 스레드에서 읽기 쓰기 모두 이용할 수 있다. (CAS)  
synchronized 경우도 여러 스레드에서 읽기 쓰기 모두 이용할 수 있다. (Lock)  
####[What is the difference between atomic / volatile / synchronized?](https://stackoverflow.com/questions/9749746/what-is-the-difference-between-atomic-volatile-synchronized)



