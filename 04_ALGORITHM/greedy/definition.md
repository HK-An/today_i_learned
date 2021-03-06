# Greedy Algorithm(탐욕 알고리즘)

## 개요
탐욕 알고리즘은 현재 선택할 수 있는 선택지에서 최적이라고 생각되는 것을 선택해나가는 방식으로 진행하여 최종적인 해답에 도달한다. 순간마다 하는 선택은 그 시점에서는 최적이지만, 전체를 봤을때 최적임을 보장하지는 않는다.

## 탐욕 알고리즘이 적용되기 위한 조건
<img src="https://ifh.cc/g/K8CK9A.png">

### 탐욕스러운 선택 조건(Greedy choice Property)
앞의 선택이 앞으로의 선택과 무관하여야 한다. 한번 선택한 것을 버리고 다른 값을 취하거나 하지 않는다.  
위의 다이어그램을 탐욕알고리즘으로 탐색할 경오 3->14->4의 경로로 도달하게 되는데, 마지막 노드에 도달할 경우 최댓값이 아닌걸 깨닫고 다시 최초 노드로 돌아가거나 하는 등 [깊이우선탐색](https://github.com/HK-An/today_i_learned/blob/main/ALGORITHM/DFS/definition.md)과 같은 과정으로 진행되면 안된다.

### 최적 부분 구조 조건(Optimal substructure)
 부분적인 최적해가 문제 전체의 관점에서도 최적해이어야 한다. 현재시점이 전체적인 관점에서도 최적의 선택이 되어야 한다.  
위의 그림을 탐욕 알고리즘으로 탐색 할 경우 3->14->4의 경로로 도달하게 되는데, 모두 합할 경우 최댓값인 41에 도달하지 못하였기 때문에 이와 같은 자료에서는 탐욕 알고리즘을 적용할 수 없다.

## 장점
- 계산 속도가 빠르다.
- 구현이 단순하다.

## 단점
- 위의 조건에 만족하지 않는 경우에는 최적해를 구하지 못한다.
- 위의 이유로 굉장히 제한적인 상황에서만 사용이 가능하다.


##### 출처
> https://ko.wikipedia.org/wiki/%ED%83%90%EC%9A%95_%EC%95%8C%EA%B3%A0%EB%A6%AC%EC%A6%98  
>
