#[Command Line Interface](https://www.vagrantup.com/docs/cli/)

###vagrant box add
Box 다운로드  

`vagrant box add ubuntu/trusty64`  
~.vagrant.d/boxes 에 저장되고 `vagrant up`에서 사용함. 없으면 온라인에서 찾는듯

###vagrant box list
Box 이미지 카탈로그 조회  

###vagrant init
```
vagrant init centos/7  
vagrant init
```
vagrant 프로젝트 디렉토리 초기화  
init 과 함께 초기화 os 지정할 수 있음

###vagrant ssh
ssh 접근

###vagrant status
vagrant 인스턴스 상태확인

###vagrant global-status
호스트 머신 전체의 Vagrant 가상 이미지들의 상태 확인

###vagrant reload
변경된 VagrantFile 적용

###vagrant halt
가상 인스턴스 강제 종료

###vagrant destroy
가상 이미지 종료 및 기존 이미지 삭제

###vagrant suspend
가상 인스턴스 하이버네이트, 상태 보존

###vagrant resume
중지된 인스턴스 시작

###vagrant reload
변경된 VagrantFile 적용


###vagrant provision
게스트머신 설정 변경하고 적용?