---
layout: single
title: SolrCloud 설치
comments: true
categories: Solr SolrCloud
tags:
- from
- white space
---

# 가나다라마바사 abcd ABCD

## 가나다라마바사 abcd ABCD

### 가나다라마바사 abcd ABCD

#### 가나다라마바사 abcd ABCD

##### 가나다라마바사 abcd ABCD
###### 가나다라마바사 abcd ABCD
####### 가나다라마바사 abcd ABCD

```
  public aaa(){
  }
```
zookeeper

zookeeper 의 leader clustor 정의
 * data 폴더 생성
 * data/myid 생성
 * data/myid 
    > 1 #contents
 
zoo.cfg 생성
 * conf/zoo.cfg
    > tickTime=2000 
    > dataDir=/home/zookeeper-3.4.10/data 
    > clientPort=2181 
    > initLimit=5 
    > syncLimit=2 
    > server.1=192.168.10.154:2888:3888 

zookeeper 실행
server.X 가 있는 zookeeper들을 모두 실행
/home/zookeeper-3.4.10/bin/zkServer.sh start

zookeeper 상태 확인
/home/zookeeper-3.4.10/bin/zkServer.sh status



solr
 * example, docs 삭제

/home/solr-7.2.1/bin/solr start -cloud -z 192.168.10.154:2181 -force -p 8390
/home/solr-7.2.1/bin/solr create -c unus-collection -shards 4 -replicationFactor 3 -force


















