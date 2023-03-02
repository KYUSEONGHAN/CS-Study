![](https://www.python.org/static/community_logos/python-logo-master-v3-TM-flattened.png)

## List
- 가변 객체(데이터 타입)
- 리스트가 더 많은 메모리를 소모 (튜플에 비해)
- 리스트가 삽입과 삭제같은 프로그래밍 작업을 수행하는데 더 수월하다.
- 이터레이션(반복)을 사용함으로써 시간을 소모
- len(a) -> O(1)
- a[i] -> O(1)
- a[i:j] -> O(k) (i부터 j까지 k개)
- a.append(i) -> O(1)
- a.pop() -> O(1)
- min(a), max(a) -> O(n)

## Tuple
- 튜플은 불변 객체(데이터 타입)
- 튜플은 리스트보다 더 적은 메모리를 소모한다
- 튜플 데이터타입이 요소들에 접근하기에 더 적절하다
- 이터레이션(반복) 사용이 더 빠르다.

## 참고자료 출처
[https://dev-jacob.tistory.com/entry/%ED%8C%8C%EC%9D%B4%EC%8D%AC-%EB%A9%B4%EC%A0%91-%EC%A7%88%EB%AC%B8-%EB%A6%AC%EC%8A%A4%ED%8A%B8-1](https://dev-jacob.tistory.com/entry/%ED%8C%8C%EC%9D%B4%EC%8D%AC-%EB%A9%B4%EC%A0%91-%EC%A7%88%EB%AC%B8-%EB%A6%AC%EC%8A%A4%ED%8A%B8-1)