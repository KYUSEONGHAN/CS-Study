![](https://t1.daumcdn.net/cfile/tistory/996E34335B90DB8F20)

## Graph
- Graph = node + edge
- 비선형 자료구조
- node는 데이터를 의미
- edge는 data간의 관계를 의미하며 선으로 표현
- 대부분의 알고리즘은 입력 데이터가 유클리드 공간에 있다고 가정한다.
- 데이터의 의미와 같이 벡터의 형태로 표현 가능해야 한다.
- 비유클리드 공간의 데이터들은 오브젝트간의 복잡한 관계나 상호의존성등을 정의할 수 있는 그래프로 표현 할 수 있다.

## 그래 표현 방법
- 인접 리스트
- 인접 행렬
- feature matrix

## 인접행렬
![](https://blog.kakaocdn.net/dn/Gdb5O/btqURuGMoog/kmiBcgGSYFtYrs4Lrjepi0/img.png)
- 그래프에서 각 정점의 연결 관계, 즉 간선의 존재 여부를 행렬로 표현한 것.
- 그래프에서 정점이 N개일 때, 각 정점을 행과 열로 하는 nc차 정사각행렬.