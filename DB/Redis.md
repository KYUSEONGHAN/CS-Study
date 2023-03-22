![](https://cdn-3.backendless.com/wp-content/uploads/2022/12/How-Redis-typically-works.png)

## Redis
- 빠른 오픈 소스 인 메모리 키 값 데이터 구조 스토어
- key, value 구조의 비정형 데이터를 저장하고 관리하기 위한 오픈 소스 기반의 비관계형 데이터 베이스관리 시스템
- 데이터베이스, 캐시, 메세지 브로커로 사용되며 인메모리 데이터 구조를 가진 저장소

## Redis 특징
- key, value 구조이기 때문에 쿼리를 사용할 필요가 없다
- 데이터를 디스크에 쓰는 구조가 아니라 메모리에서 데이터를 처리하기 때문에 속도가 빠르다
- String, List, Set, Sorted Set, Hash 자료 구조를 지원
- Single Threaded 이다
    - 한 번에 하나의 명령만 처리할 수 있습니다. 그렇기 때문에 중간에 처리 시간이 긴 명령어가 들어오면 그 뒤에 명령어들은 모두 앞에 있는 명령어가 처리될 때까지 대기가 필요합니다.
    
## Redis 사용 주의점
- 서버에 장애가 발생했을 경우 그에 대한 운영 플랜이 필요하다
 - 인메모리 데이터 저장소의 특성상, 서버에 장애가 발생했을 경우 데이터 유실이 발생할 수 있기 때문입니다.
- 메모리 관리가 중요
- 싱글 스레드 특성상, 한 번에 하나의 명령만 처리할 수 있다
- 처리하는데 시간이 오래 걸리는 요청, 명령은 피해야 한다

## Redis는 언제 사용하는가?
- DB, Cache, Message Queue, Shared Memory 용도로 사용될 수 있다. 주로 Cache 서버를 구현할 때 많이 쓴다.

## Redis는 왜 Thread Safe 한가?
- 싱글 스레드 방식이어서 연산을 하나씩 처리한다

## Redis는 영속성을 어떻게 보장하는가?
- RDB 또는 AOF 방식을 통해 영속성을 보장한다.
- RDB(Snapshotting) 방식
    - 순간적으로 메모리에 있는 내용 전체를 디스크에 옮겨 담는 방식
- AOF(Append On File) 방식
    - Redis의 모든 write/update 연산 자체를 모두 log 파일에 기록하는 형태

## Redis와 Memcached의 차이는 무엇인가?
![](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FbBUbzk%2FbtrrEUM0nE8%2FE6w2P9XsgeHvgZxn9uXg00%2Fimg.png)

## 참고자료 출처
[https://steady-coding.tistory.com/586](https://steady-coding.tistory.com/586)