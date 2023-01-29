![](https://t1.daumcdn.net/cfile/tistory/9923A9505E2F133608)

## Java 문자열
- 자바에서 문자열을 다루는 대표적인 클래스로 String, StringBuffer, StringBuilder가 있다.
- 연산횟수가 많아지거나 멀티쓰레드, Race Condition 등의 상황이 자주 발생한다면 적절한 클래스를 사용해야한다.

## String
![](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Ft1.daumcdn.net%2Fcfile%2Ftistory%2F99948B355E2F13350F)
- String은 불변(immutable)의 속성을 갖는다.
- 변하지 않는 문자열을 자주 읽어들이는 경우 String을 사용하면 좋은 성능을 기대할 수 있다.
- 그러나 문자열 추가, 수정, 삭제 등의 연산이 빈번하게 발생하는 알고리즘에 String 클래스를 사용하면 힙 메모리(Heap)에 많은 가비지(Garbage)가 생성되어 힙메모리가 부족으로 어플리케이션 성능에 치명적인 영향을 끼친다.

## StringBuffer
![](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Ft1.daumcdn.net%2Fcfile%2Ftistory%2F9923A9505E2F133608)
- 가변, 동일 객체내에서 문자열 변경가능

## StringBuilder
- 가변, 동일 객체내에서 문자열 변경가능

## StringBuffer Vs StringBuilder
- 동기화의 유무
- StringBuffer
    - 동기화 키워드를 지원하여 멀티쓰레드 환경에서 안전
- StringBuilder
    - 동기화를 지원하지 않기때문에 멀티쓰레드 환경에서 사용하는 것은 적합하지 않지만 동기화를 고려하지 않은 만큼 단일쓰레드에서의 성능은 StringBuffer보다 뛰어나다.
    
## 정리
![](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Ft1.daumcdn.net%2Fcfile%2Ftistory%2F99BE23375E2F133722)
- String
    - 문자열 연산이 적고 멀티쓰레드 환경일 경우
- StringBuffer
    - 문자열 연산이 많고 멀티쓰레드 환경일 경우
- StringBuilder
    - 문자열 연산이 많고 단일쓰레드이거나 동기화를 고려하지 않아도 되는 경우

## 참고자료 출처
[https://ifuwanna.tistory.com/221](https://ifuwanna.tistory.com/221)