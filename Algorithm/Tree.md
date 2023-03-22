![](https://www.geeksforgeeks.org/wp-content/uploads/binary-tree-to-DLL.png)

## Tree 자료구조
- node와 edge로 이루어진 자료구조
- 트리는 값을 가진 노드와 이 노드들을 연결해주는 간선으로 이루어져 있다
- 그림 상 데이터 1을 가진 노드가 루트 노드 이다
- 모든 노드들은 0개 이상의 자식 노드를 가지고 있으며 보통 부모-자식 관계로 부른다

## 트리 특징
- 트리에는 사이클이 존재할 수 없다
- 만약 사이클이 만들어진다면, 그것은 트리가 아니고 그래프이다
- 모든 노드는 자료형으로 표현이 가능하다
- 루트에서 한 노드로 가는 경로는 유일한 경로 뿐이다
- 노드의 개수가 n개면, 간선은 n-1개이다

## 트의와 그래프의 차이점
- 사이클의 유무
    - 트리: 사이클 x
    - 그래프: 사이클 o

## 트리 순회 방식
1. 전위 순회 (pre-order)
2. 중위 순회 (in-order)
3. 후위 순회 (post-order)
4. 레벨 순회 (level-order)

## 전위 순회
- pre order
- 각 루트를 순차적으로 먼저 방문하는 방식
- root > 왼쪽 자식 > 오른쪽 자식
- 1 → 2 → 4 → 8 → 9 → 5 → 10 → 11 → 3 → 6 → 13 → 7 → 14

## 중위 순회
- in order
- 왼쪽 하위 트리를 방문 후 루트를 방문하느 방식
- 왼쪽 자식 > root > 오른쪽 자식
- 8 → 4 → 9 → 2 → 10 → 5 → 11 → 1 → 6 → 13 → 3 →14 → 7

## 후위 순회
- post order
- 왼쪽 하위 트리부터 하위를 모두 방문 후 루트를 방문하는 방식
- 왼쪽 자식 > 오른쪽 자식 > root
- 8 → 9 → 4 → 10 → 11 → 5 → 2 → 13 → 6 → 14 → 7 → 3 → 1

## 레벨 순회
- Level order
- 루트부터 계층 별로 방문하는 방식
- 1 → 2 → 3 → 4 → 5 → 6 → 7 → 8 → 9 → 10 → 11 → 13 → 14

## 참고자료 출처
[https://gyoogle.dev/blog/computer-science/data-structure/Tree.html](https://gyoogle.dev/blog/computer-science/data-structure/Tree.html)