![](https://i.ytimg.com/vi/4wVp97-uqr0/maxresdefault.jpg)

## LRU 알고리즘
- least recently used algorithm
- 가장 오랫동안 참조되지 않은 페이지를 교체하는 기법

## 장점
- 빠른 액세스
    - 가장 최근에 사용한 아이템부터 가장 적에 사용한 아이템까지 정렬된다.
    - 따라서 두 아이템에 접근할 경우, O(n)의 시간 복잡도를 가진다.
- 빠른 업데이트
    - 하나의 아이템에 액세스 할때마다 업데이트 되며, O(n)의 시간 복잡도를 가진다.

## LRU 알고리즘 단점
- 프로세스가 주기억장치에 접급할 때마다 참조된 페이지에 대한 시간을 기록해야함
- 큰 오버헤드가 발생
- 많은 공간 차지


## LRU 알고리즘 설명
![](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Ft1.daumcdn.net%2Fcfile%2Ftistory%2F998933375C7F78A428)
- Input : 123145
- Output : 5413

## 페이지 교체 알고리즘
- 페이지 교체 알고리즘은 페이징 기법으로 메모리를 관리하는 운영체제에서, 페이지 부재가 발생하여 새로운 페이지를 할당하기 위해 현재 할당된 페이지 중 어느 것과 교체할지를 결정하는 방법이다.

## 페이지 교체 알고리즘 종류
- FIFO
    - 페이지가 주기억장치에 적재된 시간을 기준으로 교체될 페이지를 선정하는 기법
- LFU
    - 가장 적은 횟수를 참조하는 페이지를 교체
- LRU
    - 가장 오랫동안 참조되지 않은 페이지를 교체

## LRU python code
```python
cacheSize = 3
reference = [4, 2, 3, 4, 5, 6, 5, 4, 7]
cache = []
for ref in reference:
  if not ref in cache:
    if len(cache) < cacheSize:
        cache.append(ref)
     else:
        cache.pop(0)
        cache.append(ref)
  else:
    cache.pop(cache.index(ref))
    cache.append(ref)
```

## 참고자료 출처
[https://j2wooooo.tistory.com/121](https://j2wooooo.tistory.com/121)