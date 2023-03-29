![](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcR9SdF_Qxh81CaQsPtxXMLjPLvpZNahC1MMbg&usqp=CAU)

## Deadlock
- 교착 상태
- 프로세스가 자원을 얻지 못해서 다음 처리를 하지 못하는 상태를 뜻한다
- 두 개 이상의 작업이 서로 작업이 끝나기만을 기다리고 있기 때문에 결과적으로 아무것도 완료되지 못하는 상태
- 다중 프로그래밍 환경에서 흔히 발생

## 교착 상태의 조건
![](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FZlgCK%2Fbtrmhvlm0c4%2FzflYLbhK0K2QTOzc6f07zK%2Fimg.png)
- 우선 발생하는 이유를 간단히 살펴 보자면, Process 1과 Process 2 각각 Resource 1과 Resource 2가 필요한 상황이 있다고 하자.
- Process 1은 Resource 1을 먼저 요청하여 얻고, Process 2는 Resource 2를 먼저 요청하여 얻은 이후 Process 1은 Resource 2를 요청하지만 Process 2가 사용하여 얻을 수 없다. 
- 마찬가지로 Process 2도 Resource 1을 요청하지만 Process 1이 요청하여 서로 무한정 wait이 된다.

## 발생조건
- 상호 배제
- 점유 대기
- 비선점
- 순환 대기

## 상호 배제
- 자원은 한 번에 한 프로세만 사용할 수 있다.
- 공유 불가능한 자원의 동시 사용을 피하기 위해 특정 알고리즘을 사용한다

## 상호 배제는 어디서 구현하는가?
- 임계 구역으로 불리는 코드 영역에서 구현

## 면접 질문: 데드락이란?

## 면접 질문: 데드락이 발생하는 조건은?
- 조건 상호 배제, 점유 대기, 비선점, 순환 대기. 총 4가지 조건이 만족 되어야하며, 하나라도 만족하지 못하면 교착 상태가 발생하지 않는다. 
- 상호 배제는 자원은 한번에 한 프로세스만 사용할 수 있다는 조건
- 점유 대기는 프로세스가 할당된 자원을 가진 상태에서 다른 자원을 기다리고 있다는 조건
- 비선점은 다른 프로세스에 할당된 자원은 사용이 끝날 때 까지 강제로 빼앗을 수 없다는 조건
- 순환 대기는 각 프로세스는 순환적으로 다음 프로세스가 요구하는 자원을 가지고 있다는 조건이다.

## 면접 질문: 데드락을 해결할 수 있는 방법에는 어떤것이 있는가?
- 예방
    - 교착 상태의 4가지 조건 부정
- 회피
    - 자원 할당 그래프 알고리즘
    - 은행원 알고리즘
- 탐지
    - 대기 그래프
    - Shoshani & Coffman 알고리즘
- 회복
    - 프로세스 종료법
    - 자원 선점법

## 참고자료 출처
[https://steady-coding.tistory.com/520](https://steady-coding.tistory.com/520)