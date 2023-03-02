![](https://www.python.org/static/community_logos/python-logo-master-v3-TM-flattened.png)

## append
- array.append(x)의 형태로 사용한다.
- x를 array의 맨 끝에 객체로 추가한다.
- x가 iterable 자료형이더라도 전체를 하나의 객체로해서 요소로 추가한다.
- O(1)

## insert
- array.insert(i, x) 형태로 사용한다.
- 원하는 위치 i에 x를 삽입할 수 있다.
- 값 x는 객체로 추가된다.
- append 함수와 마찬가지로 iterable 자료형이더라도 하나의 요소로 삽입된다.
- O(N)

## extend
- array.extend(iterable) 형태로 사용한다
- iterable의 각 요소를 하나씩 array의 끝에 요소로 추가한다.
- append 함수와 다른 점은 괄호 안에 iterable 자료형만 올 수 있다.
- O(len(…))  (확장 길이에 따라)

## 참고자료 출처
[https://ooyoung.tistory.com/117](https://ooyoung.tistory.com/117)