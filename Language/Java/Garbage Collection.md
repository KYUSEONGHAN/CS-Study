![](https://tecoble.techcourse.co.kr/static/bada49a3395d2b1adaede46a24505ef0/c05c3/jvm-garbage-collection.png)

## Abstaract
- C 프로그래밍을 할 때 메모리 누수(memory leak)을 막기 위해 객체를 생성한 후 사용자하지 않는 객체의 메모리를 프로그래머가 직접 해애 해주어야 했다.
- 하지만, java에서는 JVM이 구성된 JRE가 제공되며, 그 구성 요소 중 하나인 Garbage Collection이 자동으로 사용하지 않는 객체를 파괴합니다.
- GC에 알아보기 전에 `stop-the-world`란느 용어를 알아야한다.
- stop-the-word
    - GC를 싱행하기 위해 JVM이 애플리케이션 실행을 멈추는 것.
    - 어떤 GC 알고리즘을 사용하더라도 `stop-the-world`는 발생하게 되는데, 대개의 경우 GC 튜닝은 이 `stop-the-world` 시간을 줄이는 것이다.
- 따라서 자바 애플리케이션을 효율적으로 개발하기 위해서는 GC를 잘 알아야한다.

## Garbage Collection
- C/C++ 언어와 달리 자바는 개발자가 명시적으로 객체를 해재할 필요가 없다.
- 이는 자바 언어의 장점 중 하나
- 기본적으로 JVM의 메모리는 총 5가지 영역(class, stack, heap, native method, pc)으로 나누는데, GC는 힙 메모리만 다룬다.
- 일반적으로 다음과 같은 경우에 GC의 대상이 된다.
    - 객체가 NULL인 경우
    - 블럭 실행 종료 후, 블럭 안에서 생성된 객체
    - 부모 객체가 NULL인 경우, 포함하는 자식 객체

## GC 메모리 해제 과정
- Marking
- Normal Deletion
- Compacting

## 참고자료 출처
[https://gyoogle.dev/blog/computer-language/Java/Garbage%20Collection.html](https://gyoogle.dev/blog/computer-language/Java/Garbage%20Collection.html)