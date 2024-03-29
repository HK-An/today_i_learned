# 알고리즘
## 목차
1. [BFS](https://github.com/HK-An/today_i_learned/tree/main/04_ALGORITHM#1-bfs)
2. [DFS](https://github.com/HK-An/today_i_learned/tree/main/04_ALGORITHM#2-dfs)
3. [백트래킹](https://github.com/HK-An/today_i_learned/tree/main/04_ALGORITHM#3-백트래킹)
4. [시뮬레이션](https://github.com/HK-An/today_i_learned/tree/main/04_ALGORITHM#4-시뮬레이션)
5. [투포인터](https://github.com/HK-An/today_i_learned/tree/main/04_ALGORITHM#5-투포인터)
6. [이진탐색](https://github.com/HK-An/today_i_learned/tree/main/04_ALGORITHM#6-이진탐색)
7. [그리디](https://github.com/HK-An/today_i_learned/tree/main/04_ALGORITHM#7-그리디)
8. [다이나믹프로그래밍](https://github.com/HK-An/today_i_learned/tree/main/04_ALGORITHM#8-다이나믹프로그래밍)
9. [MST](https://github.com/HK-An/today_i_learned/tree/main/04_ALGORITHM#9-mstminimum-spanning-tree)
10. [다익스트라](https://github.com/HK-An/today_i_learned/tree/main/04_ALGORITHM#10-다익스트라)

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
> **O (V+E)**  

### 구현을 위해 필요한 자료구조
1. 검색할 그래프
2. 방문여부 확인을 위한 데이터(보통 배열)
3. Queue

### 문제링크
[문제리스트](https://solved.ac/problems/tags/bfs)  
[1926번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p1xxx/P1926.java) | [2606번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p2xxx/P2606.java) | [16173번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p16xxx/P16173.java)  
푼문제수: 총 **3**개

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
> **O (V+E)**  

### 자료구조
1. 검색할 그래프: 2차원 배열
2. 방문여부 확인: 2차원 배열

### 문제링크
[문제리스트](https://solved.ac/problems/tags/dfs)  
[1926번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p1xxx/P1926.java) | [2606번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p2xxx/P2606.java) | [16173번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p16xxx/P16173.java)  
푼문제수: 총 **3**개


[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## 3. 백트래킹
### 개요
백트래킹은 모든 경우의 수를 고려하여야 하지만, 데이터의 depth가 달라져 일반적인 반복문으로는 구현이 힘들거나 불가능할때 사용한다. DFS도 백트래킹 방법을 사용하여 구현하는 편이다.

### 시간복잡도
> - O(n^n): 탐색하는 데이터가 중복되어 탐색이 가능할 때. n=8까지 가능하다.
> - O(n!): 탐색하는 데이터가 중복되어 탐색이 불가능할때. n=10까지 가능하다.

### 문제링크
[문제리스트](https://solved.ac/problems/tags/backtracking)  
[15649번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p15xxx/P15649.java) | [15650번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p15xxx/P15650.java)  
푼문제수: 총 **2**개

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## 4. 시뮬레이션
### 개요
각 조건에 맞는 상황을 구현하는 문제
- 지도상에서 이동하면서 탐험하는 문제
- 배열안에서 이동하면서 탐험하는 문제
별도의 알고리믖 없이 풀 수있으나, 구현력이 중요함. 매 시험마다 1문제 이상 무조건 출제

### 문제링크
[문제리스트](https://solved.ac/problems/tags/simulation)  

푼문제수: 총 **0**개

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## 5. 투포인터

<img src="https://github.com/HK-An/today_i_learned/blob/main/00_IMGS/04_ALGORITHM/twoPointer.PNG">

### 개요
두개의 포인터(커서)가 움직이면서 계산한다. 특정 조건에 따라 startPointer와 endPointer를 조절하면서 원하는 범위의 값을 가져와 진행한다. 처음부터 생각하기 어려운 방법이니 처음에는 쉬운 방법으로 우선 접근하여 시간복잡도나 변수가 범위안에 들지 않을때 사용하기.

### 시간복잡도
> - O(N^2)각 원소마다 모든 값을 순회해야할때
> - O(N): 연속하다는 특성을 가지고 처리했을때

## 문제링크
[문제리스트](https://solved.ac/problems/tags/two_pointer)  
[2003번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p2xxx/P2003.java) | [2559번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p2xxx/P2559.java)  
푼문제수: 총 **2**개

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## 6.이진탐색
### 개요
어떤 값을 찾을 때 정렬의 특징을 이용해 빨리 찾는다. 가지고 있는 원소들의 절반을 나누어 찾고자 하는 값보다 큰지 작은지 판단하여 다음 탐색한다. 처음부터 생각하기 어려운 방법이니 처음에는 쉬운 방법으로 우선 접근하여 시간복잡도나 변수가 범위안에 들지 않을때 사용하기.

### 시간복잡도
> O(logN): 어떠한 값을 찾을 때

### 문제링크
[문제리스트](https://solved.ac/problems/tags/binary_search)  
[1920번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p1xxx/P1920.java)  
푼문제수: 총 **1**개

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## 7. 그리디
### 개요
현재 상황에서 찾을 수 있는 답 중 목표에 가장 근접하는 것을 찾는다. 현재의 최선의 값이 결론적으로 최선의 결과가 되지 않을수도 있다. 그러므로 그리디를 이용하여 문제를 풀기 위해서는 각 상황에서 선택하는 것들이 결론적으로도 최선임을 증명할 수 있어야 하며, 이를 찾는 연습을 하는것이 중요하다.

### 문제링크
[문제리스트](https://solved.ac/problems/tags/greedy)  
[11047번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p11xxx/P11047.java)  
푼문제수: 총 **1**개

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## 8. 다이나믹프로그래밍
### 개요
경우의 수를 반복하며 이전경우에서 구한 값을 재활용 하는 알고리즘이다. 단순 반복하는 것보다 이전 값을 사용할 수 있는 상황에서 이전 값을 이용하여 값을 구할 경우 시간복잡도를 줄일 수 있다. DP를 사용하기 위해서는 꼭 점화식을 짜야하며, 문제를 보자마자 점화식을 찾을 수는 없으니, 하나씩 답을 구해가며 각 답을 구할 수 있는 점화식의 규칙성을 찾고 해당 점화식을 이용하여 코드를 짜야한다.

### 문제링크
[문제리스트](https://solved.ac/problems/tags/dp)  
[11726번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p11xxx/P11726.java)  
푼문제수: 총 **1**개

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## 9. MST;Minimum Spanning Tree
### 개요
Spanning Tree란 누락없이 모든 노드가 연결된 트리를 의미한다. MST는 현재 각 Vertex끼리 양방향으로 가중치를 가진 간선으로 연결된 그래프에서 최소의 가중치합으로 Spanning Tree를 만드는 것을 의미한다.

### 방법
MST를 푸는 방법으로는 다음의 두가지가 있다.
1. Kruskal 전체 간선 중 비용이 작은것부터 순서대로 연결한다.
2. Prim 현재 연결된 트리에 이어진 간선 중 비용이 가장 적은것을 추가한다. 이때 heap 자료 구조를 사용한다.

### 시간복잡도
> O(ElogE)

### 문제링크
[문제리스트](https://solved.ac/problems/tags/mst)  
[1197번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p1xxx/P1197.java)  
푼문제수: 총 **1**개

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## 10. 다익스트라
### 개요
한 노드에서 모든 노드(시작점에서부터 각각의 노드)까지 가는데 사용하는 최소비용을 찾는 알고리즘

### 작동원리

### 문제링크
[문제리스트](https://solved.ac/problems/tags/dijkstra)

푼문제수: 총 **0**개
