![alt icon](https://cdn.iconscout.com/icon/free/png-256/vagrant-5-1174986.png)

#ref
[공식사이트](https://www.vagrantup.com/)  
[공식 box](https://app.vagrantup.com/boxes/search)  
[Vagrant를 이용한 손쉬운 개발환경 구축](https://rorlab.org/rblogs/232)  
[Vagrant 공유 폴더 문제(mount.vboxsf 관련) - vagrant-vbguest 플러그인](https://javaworld.co.kr/96)  
[Vagrant를 이용한 개발환경 관리(간단한 VM관리)](https://bcho.tistory.com/806)  
[내컴에선 잘되던데? – vagrant로 서버와 동일한 개발환경 꾸미기](https://andromedarabbit.net/%EB%82%B4%EC%BB%B4%EC%97%90%EC%84%A0-%EC%9E%98%EB%90%98%EB%8D%98%EB%8D%B0-vagrant%EB%A1%9C-%EC%84%9C%EB%B2%84%EC%99%80-%EB%8F%99%EC%9D%BC%ED%95%9C-%EA%B0%9C%EB%B0%9C%ED%99%98%EA%B2%BD-%EA%BE%B8/)  
[vagrant box 패키징과 공유](https://oddpoet.net/blog/2014/04/11/share-vagrant-box/)  
[hef 를 이용하여 개발환경을 통일할 수 있을까?](https://java.ihoney.pe.kr/269)  


#간략설명
루비로 만들어진 가상화 인프라 구축 오픈소스 프로젝트  
부랑자라는 뜻  

제발.. 인생설정 하나 만들어서 쓰자.  
맨날 지웠다 깔고 까먹고 찾고 하지말고


#설치
[virtualbox](https://www.virtualbox.org/)  
[vagrantup](https://www.vagrantup.com/)  

```
vagrant plugin install vagrant-vbguest    
vagrant plugin install vagrant-librarian-chef-nochef
```
>가상화 공유 오류때문에 설치하는다는데 정확히 모름




---

vagrant vm 놓을 폴더로 이동
`vagrant init`

---

Vagrantfile 편집
>생성될 vm 세부사항 정의
>vm(up, reload, provision)이 기동될때 마다 실행된다. 설치됬으면 설치안하는 스크립트로 작성하는게 좋음


```
[Vagrantfile](https://github.com/zsgg/vagrant/blob/master/vm/Vagrantfile)
```

---

시동
`vagrant up`

---


게스트 접속
`vagrant ssh`


---

####공유폴더
```
cd "D:/LocalDev/vm"
vagrant up
vagrant ssh
```
위와 같이 설치했다면, 게스트머신 /vagrant 폴더는 vm 폴더와 공유된다. 
 
