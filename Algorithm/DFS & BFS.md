![](https://images.velog.io/images/stat_wkon/post/b7a36854-cf23-4238-9453-f928d92ef321/BFS,DFS.png)

## DFS & BFS
- 그래프 알고리즘으로, 경로를 찾는 문제일 시 상화에 맞게 활용하면 된다.

## DFS
- 루트 노드 혹은 임의 노드에서 다음 브랜치로 넘어가기 전에, 해당 브랜치를 모두 탐색하는 방법
- 스택 or 재귀함수를 통해 구현
- 모든 경로를 방문해야 할 경우 적합하다
- 시간 복잡도
    - 인접 행렬: o(v^2)
    - 인접 리스트: o(v+e)
    - v는 접점, e는 간선을 의미

## BFS
- 루트 노드 또는 임의 노드에서 인접한 노드부터 먼저 탐색하는 방법
- 큐를 통해 구현 (해당 노드의 주변부터 탐색해야 해서)
- 최소 비용(즉, 모든 곳을 탐색하는 것보다 최소 비용이 우선일 때)에 적합
- 시간 복잡도
    - 인접 행렬: o(v^2)
    - 인접 리스트: o(v+e)
- 최소 이동 등을 구할땐 BFS가 유리하며, list에 증감하면서 접근하자.
<img width="525" alt="스크린샷 2023-01-28 오후 4 35 25" src="https://user-images.githubusercontent.com/82144756/215253545-5c448c6a-177f-4028-b706-25e5dc67babd.png">

## 참고자료 출처
[https://velog.io/@stat_wkon/TIL-2-BFS%EC%99%80-DFS-%EC%9D%B4%ED%95%B4](https://velog.io/@stat_wkon/TIL-2-BFS%EC%99%80-DFS-%EC%9D%B4%ED%95%B4)