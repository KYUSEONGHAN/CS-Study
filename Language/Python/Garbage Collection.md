![](https://www.askpython.com/wp-content/uploads/2020/08/Garbage-Collection-in-Python.png)

## Garbage Collector
- OS는 프로그램을 프로세스로 실행하게 되고, 해당 프로세스는 메모리에 코드, 데이터, 힙, 스택 영역을 할당받게 된다.
- 이 때, 힙, 스택 영역에 할당된 메모리들을 해제하는 동작을 Garbage Collector가 수행하게 된다.

## Python GC
- python에서는 GC를 다음 2가지 방식으로 동작한다
    - Reference counting
    - generational garbage collection
    
## Reference Counting
```python
import sys
a = 'hello'
sys.getrefcount(a)  # 2
```
- 레퍼런스 카운팅 방식의 가비지 컬렉팅은, 어떤 객체가 참조되고있는 횟수를 카운팅하고 0이 될 경우 메모리에서 해제하는 방식이다.
- python standard library의 sys모듈로 특정 객체의 reference counts를 확인할 수 있다.
- 위 코드에서, 'hello'는 힙에 할당되고 a는 지역변수라는 가정 하에 스택에 할당되어 'hello'가 위치한 힙의 주소를 갖고 있다.
- 이 상황에서 a의 레퍼런스 카운트는 2이다.
- 첫번째는 a가 위치한 스택의 주소가 콜스택에서 참조되고 있기 때문이며, 두번째는 getrefcount()에 전달될 때이다.
- 만약 콜스택에서 a가 위치한 레벨의 함수가 실행 완료되면, 콜스택에서 참조하고 있는 a가 사라지기에 reference count는 0이되고 gc에 의해 메모리에서 해제된다.

## Generational GC
```python
l = []
l.append(l)
del l
```
- 위 코드의 l과 같이, 만약 어떤 동적 객체가 서로를 참조(순환참조)하고 있다면 Reference counting 방식에서는 해당 객체들은 메모리에서 해제될 수 없다.
- 이러한 경우를 방지하기 위해, 파이썬에서는 Generational garbage collection이 순환 참조를 탐지하고 메모리에서 해제해준다.

## 참고자료 출처
[https://velog.io/@zihs0822/Python%EC%9D%98-GC%EC%99%80-GIL](https://velog.io/@zihs0822/Python%EC%9D%98-GC%EC%99%80-GIL)
