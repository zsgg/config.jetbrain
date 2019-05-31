#OpenSSL
###[Creative IT - IT에 창의력을 그리다 : 네이버 블로그](http://ysw1130.blog.me/120211395594)
###[Secure programming with the OpenSSL API](https://www.ibm.com/developerworks/linux/library/l-openssl/index.html)
웹브라우저와 서버간의 통신을 암호화하는 오픈소스

------

#ssl : Secreat Socket Layer
###[[정보보안] SSL(Secure Socket Layer) 이란](http://12bme.tistory.com/80)
SSL의 핵심은 암호화입니다. SSL은 보안과 성능상의 이유로 두가지 암호화 기법을 혼용해서 사용하고 있는데, SSL 동작방법을 이해하기 위해서는 이 암호화 기법들에 대한 이해가 필요합니다.

#####대칭키
대칭키는 동일한 키로 암호화와 복호화를 같이 할 수 있는 방식의 암호화 기법을 의미합니다.

#####공개키
공개키 방식은 두개의 키를 갖게 되는데 A키를 암호화를 하면 B키로 복호화할 수 있고, B키로 암호화하면 A키로 복호화할 수 있는 방식입니다. 이 방식에 착안해서 두개의 키 중 하나를 비공개키(private key, 개인키, 비밀키라고도 부릅니다)로 하고, 나머지를 공개키(public key)로 지정합니다.  
공개키가 데이터를 제공한 사람의 신원을 보장해주게 되는 것입니다. 이러한 것을 전자 서명이라고 부릅니다.

#####todo ssl flow

------


#ssh : Secure SHell
###[시큐어 셸](https://ko.wikipedia.org/wiki/%EC%8B%9C%ED%81%90%EC%96%B4_%EC%85%B8)
###[SSH   Secure Shell](http://www.ktword.co.kr/abbr_view.php?m_temp1=2524)
SSH는 원격 컴퓨터에 안전하게 액세스하기 위한 유닉스 기반의 명령 인터페이스 및 프로토콜. SSH는 네트웍 관리자들이 웹서버를 포함한 여러 종류의 원격지에서 제어하기 위해 널리 사용된다.

SSH는 Secure Shell의 약자입니다. SSH는 한마디로 정의하면, 네트워크 상의 다른 컴퓨터에 로그인하거나 원격 시스템에서 명령을 실행하고 다른 시스템으로 파일을 복사할 수 있도록 해 주는 프로토콜입니다. VPN을 구성하는 것보다 가격이 저렴하고 쉽게 연결할 수 있어 많이 사용됩니다.

MacOS에는 OpenSSH 클라이언트와 서버가 내장되어 있기 때문에 바로 사용할 수 있습니다.   
SSH는 22번 포트 를 사용.

------

#https
#####[HTTPS와 SSL 인증서 - 생활코딩](https://opentutorials.org/course/228/4894)
#####[SSL이란 무엇이며 인증서(Certificate)란 무엇인가?](https://wiki.kldp.org/HOWTO/html/SSL-Certificates-HOWTO/x70.html)







