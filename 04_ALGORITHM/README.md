# 알고리즘
## 목차
1. [BFS](https://github.com/HK-An/today_i_learned/tree/main/04_ALGORITHM#1-bfs)
2. [DFS](https://github.com/HK-An/today_i_learned/tree/main/04_ALGORITHM#2-dfs)
3. [백트래킹](https://github.com/HK-An/today_i_learned/tree/main/04_ALGORITHM#2-백트래킹)

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

## 2. DFS
> DFS;Depth-First Search 깊이 우선 탐색

### 개요
DFS는 데이터가 트리 혹은 그래프일때, 최상위 노드에서 자식 노드를 우선으로 하여 가장 깊은 노드까지 탐색하는 알고리즘을 의미한다.

### 흐름
- 시작점에 연결된 Vertex를 찾는다.
- 연결된 Vertex를 계속해서 찾는다. (끝날때까지)
- 해당 노드에 연결된 Vertex가 없을때까지 다음노드를 찾는다.

### 시간복잡도
>V: Vertex의 수  
E: Edge의 수

**O (V+E)**  

### 자료구조
1. 검색할 그래프: 2차원 배열
2. 방문여부 확인: 2차원 배열

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## 3. 백트래킹
### 개요
백트래킹은 모든 경우의 수를 고려하여야 하지만, 데이터의 depth가 달라져 일반적인 반복문으로는 구현이 힘들거나 불가능할때 사용한다. DFS도 백트래킹 방법을 사용하여 구현하는 편이다.

### 시간복잡도
> - n^n: 탐색하는 데이터가 중복되어 탐색이 가능할 때. n=8까지 가능하다.
- n!: 탐색하는 데이터가 중복되어 탐색이 불가능할때. n=10까지 가능하다.

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />
