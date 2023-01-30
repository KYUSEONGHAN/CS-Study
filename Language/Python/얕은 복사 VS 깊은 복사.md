![](https://images.velog.io/images/ksung1889/post/4b1040a4-e7ff-4348-8411-cf7dc8616558/image.png)

## 얕은 복사
- shallow copy
- copy 모듈의 copy 메소드 또한 얕은 복사
- 얕은 복사는 대입(=), [:] 슬라이싱, 객체.copy, copy.copy 가 ㅇㅆ다.
```python
>>> import copy
>>> a = [[1,2],[3,4]]
>>> b = copy.copy(a)
>>> a[1].append(5)
>>> a
[[1, 2], [3, 4, 5]]
>>> b
[[1, 2], [3, 4, 5]]
```

## 깊은 복사
- 깊은 복사는 내부에 객체들까지 모두 새롭게 copy되는 것이다.
- copy.deepcopy 메소드가 해결
```python
>>> import copy
>>> a = [[1,2],[3,4]]
>>> b = copy.deepcopy(a)
>>> a[1].append(5)
>>> a
[[1, 2], [3, 4, 5]]
>>> b
[[1, 2], [3, 4]]
```

## 얕은 복사와 깊은 복사
- 얕은 복사는 객체를 새로운 객체로 복사하지만 원복 객체의 주소값을 복사 -> 원본 배열 값 변경됨
- 깊은 복사는 전체 복사로 참조값의 복사가 아닌 참조된 객체 자체를 복사하는것 -> 원본 배열 보존됨, 값 변경 X

## 참고자료 출처
[https://wikidocs.net/16038](https://wikidocs.net/16038)