# 알고리즘
## 목차
1. [BFS](https://github.com/HK-An/today_i_learned/tree/main/04_ALGORITHM#1-bfs)
2. [DFS]()

<hr />


<img src="https://github.com/HK-An/today_i_learned/blob/main/00_IMGS/04_ALGORITHM/graph.PNG">

## 1. BFS
> BFS;Breadth-first search 너비 우선 탐색

### 개요
BFS는 데이터가 트리 혹은 그래프일때, 각 노드의 이웃된 노드(자식노드)부터 탐색하여 가장 깊은 노드까지 탐색하는 탐색 알고리즘을 의미한다.

### 흐름
1. 시작점에 연결된 vertex를 찾는다.
2. 찾은 vertex를 Queue에 저장한다.
3. 모든 연결된 vertex를 Queue에 저장하였으면, Queue에서 데이터를 차례대로 꺼내서 필요한 동작을 수행한다.

### 시간복잡도  
>V: Vertex의 수  
E: Edge의 수

### 구현을 위해 필요한 자료구조
1. 검색할 그래프
2. 방문여부 확인을 위한 데이터(보통 배열)
3. Queue

**O (V+E)**  

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />
