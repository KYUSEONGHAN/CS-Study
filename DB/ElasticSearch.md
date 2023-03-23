![](https://www.zen-networks.io/wp-content/uploads/2022/12/elasticsearch-1.png)

## ElasticSearch란?
- Apache Lucene(아파치 루씬) 기반의 Java 오픈소스 분산 검색 엔진이다.
- ElasticSearch를 통해 루씬 라이브러리(Java에서 개발한 정보 검색용 라이브러리)를 단독으로 사용할 수 있으며, 방대한 양의 데이터를 신속하게(거의 실시간) 저장, 검색, 분석을 수행할 수 있다
- 엘라스틱서치는 검색을 위해 단독으로 사용되기도 하며, ELK 스택으로 사용되기도 한다

## ELK Stack
- 주로 ELK는 로드밸런싱되어 있는 WAS의 흩어져 있는 로그를 한 곳으로 모으고, 원하는 데이터를 빠르게 검색한 뒤 시각화하여 모니터링하기 위해 사용한다
- Logstash
    - 다양한 소스(DB, csv 파일 등)의 로그 또는 트랜잭션 데이터를 수집, 집계, 파싱하여 Elasticsearch로 전달
- Elasticsearch
    - Logstash로부터 받은 데이터를 검색 및 집계하여 필요한 정보를 획득
- Kibana
    - Elasticsearch의 빠른 검색을 통해 데이터를 시각화 및 모니터링
    
## ElasticSearch VS RDBMS
![](https://www.notion.so/image/https%3A%2F%2Fs3-us-west-2.amazonaws.com%2Fsecure.notion-static.com%2Fade69f5c-08cb-4e45-80c3-c25e0961898a%2FUntitled.png?table=block&id=c05898df-2eca-414c-93bc-49745b486412&spaceId=b453bd85-cb15-44b5-bf2e-580aeda8074e&width=2000&userId=80352c12-65a4-4562-9a36-2179ed0dfffb&cache=v2)

## ElasticSearch VS NoSQL
- 엘라스틱 서치
    - 실시간 처리 불가능
    - 역색인 자료 구조가 있다
    - 저장소보다는 검색 엔진에 가깝다
- NoSQL
    - 실시간 처리 가능
    - 역색인 자료 구조가 없다
    
## ElasticSearch 구조
![](https://www.notion.so/image/https%3A%2F%2Fs3-us-west-2.amazonaws.com%2Fsecure.notion-static.com%2F19d4e1bf-ed80-4490-825e-405ba3dfe335%2FUntitled.png?table=block&id=132ad956-3ff3-49c7-9437-41792a20b774&spaceId=b453bd85-cb15-44b5-bf2e-580aeda8074e&width=2000&userId=80352c12-65a4-4562-9a36-2179ed0dfffb&cache=v2)
    
## 클러스터
- 클러스터란 엘라스틱서치에서 가장 큰 시스템 단위를 의미
- 최소 하나 이상의 노드로 이루어진 노드의 집합

## 노드
- 클러스터에 포함된 단일 서버로서, 데이터를 저장하고 클러스터의 색인화 및 검색 기능에 참여

## 샤드
- shard
- 인덱스 내부에는 색인된 데이터들이 존재하는데, 이 데이터들을 하나로 뭉쳐서 존재하지 않고 물리적 공간에 여러 부분으로 나뉘어 존재한다
- 이러한 부분을 샤드라고 한다
- 즉, 스케일 아웃을 위해 하나의 인덱스를 여러 샤드로 쪼갯다고 생각하면 된다

## 세그먼트
- 엘라스틱서치에서 문서의 빠른 검색을 위해 설계된 자료 구조
- 샤드의 데이터를 가지고 있는 물리적인 파일
- 각 샤드는 다수의 세그먼트로 구성되어 있으므로 검색 요청을 분산 처리하여 훨씬 효율적이 검색이 가능하다

## ElasticSearch 장점
- scale out
    - 샤드를 통해 규모가 수평적으로 늘어날 수 있다
- 고가용성
    - Replica를 통해 데이터의 안전성을 보장
- Schema Free
    - Json 문서를 통해 데이터 검색을 수행하므로 스키마 개념이 없음
- Restful
    - 데이터 CRUD 작업은 HTTP Restful API를 통해 수행한다.
        - SELECT = GET
        - INSERT = PUT
        - UPDATE = POST
        - DELETE = DELETE
        - Restful API를 사용한다는 것은 다양한 플랫폼에서 응용이 가능하다는 장점이 있다.
- 역색인

## ElasticSearch 단점
- 실시간 처리가 불가능
    - elasticsearch는 인메모리 버퍼를 사용하므로 쓰기와 동시에 읽기 작업을 할 경우, 세그먼트가 생성되기 전까지는 해당 데이터를 검색할 수 없다.
- 트래잭션을 지원하지 않는다

## 면접질문: 엘라스틱서치는 언제 사용하는가?
- Elasticsearch는 검색을 위해 단독으로 사용되기도 하며, ELK(Elasticsearch / Logstash / Kibana) 스택으로 사용되기도 한다.

## 면접질문: ELK를 왜 사용하는가
- 주로 ELK는 로드밸런싱되어 있는 WAS의 흩어져 있는 로그를 한 곳으로 모으고, 원하는 데이터를 빠르게 검색한 뒤 시각화하여 모니터링하기 위해 사용한다

## 면접질문: 엘라스틱서치 구조를 설명하라
- Elasticsearch는 클러스터로 구성되며, 클러스터 안에 노드, 노드 안에 인덱스, 인덱스 안에 샤드, 샤드 안에 세그먼트로 구성된다.

## 면접질문: 엘라스틱 서치는 왜 검색 속도가 빠른가?
- 역색인 자료 구조로 인해 빠르다.

## 면접질문: 엘라스틱서치 장단점?
- 장점 (scale out, 고가용성, schema free, restful, 역색인)
- 단점 (실시간 처리가 불가능, 트랜잭션 지원하지 않는다)

## 면접질문: 엘라스틱서치와 RDBMS의 차이
- Elasticsearch는 Json 문서를 통해 검색을 수행하므로 스키마가 없지만, RDBMS는 엄격한 스키마가 존재한다.
- Elasticsearch는 역색인 자료 구조로 검색을 수행하지만, RDBMS는 인덱스 자료 구조로 검색을 수행한다.
- Elasticsearch는 저장소보다는 검색 엔진에 가깝다.

## 면접질문: 엘라스틱서치와 nosql의 차이
- Elasticsearch는 실시간 처리가 불가능하지만, NoSQL은 실시간 처리가 가능하다.
- Elasticsearch는 역색인 자료 구조가 있지만, NoSQL은 없다.
- Elasticsearch는 저장소보다는 검색 엔진에 가깝다.

## 참고자료 출처
[https://steady-coding.tistory.com/573](https://steady-coding.tistory.com/573)