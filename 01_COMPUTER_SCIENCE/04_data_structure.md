# 자료구조
## 목차

1. [Stack](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/01_data_structure.md#stack)
  1. [스택의 특징](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/01_data_structure.md#특징)
  2. [스택의 사용 예](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/01_data_structure.md#사용예)
  3. [java에서](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/01_data_structure.md#java에서)
2. [Queue](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/01_data_structure.md#queue)
  1. [큐의 특징](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/01_data_structure.md#특징-1)
  2. [큐의 사용 예](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/01_data_structure.md#사용예-1)
  3. [java에서](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/01_data_structure.md#java에서-1)
3. [Heap](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/01_data_structure.md#heap)
  1. [힙의 특징](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/01_data_structure.md#특징-2)
  2. [힙의 사용 예](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/01_data_structure.md#사용예-2)
  3. [java에서](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/01_data_structure.md#java에서-2)
  1. [힙이 할수있는 것을 균형 이진 트리가 할수 있지않나?](
1. [이진 탐색 트리](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/01_data_structure.md#이진탐색트리)
  1. [이진탐색트리의 특징]((https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/01_data_structure.md#특징-3)
  2. [이진탐색트리의 사용 예](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/01_data_structure.md#사용예-3)
  3. [java에서](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/01_data_structure.md#java에서-3)
  1. [이진 탐색 트리 삽입, 탐색, 삭제](
1. [자가 균형 트리]()
  1. [자가균형트리의 특징]((https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/01_data_structure.md#특징-4)
  2. [자가균형트리의 사용 예](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/01_data_structure.md#사용예-4)
    1. [AVL](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/01_data_structure.md#AVL)
    1. [Red Black Tree](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/01_data_structure.md#redblacktree)
  3. [java에서](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/01_data_structure.md#java에서-4)

1. [해시]()
  1. [해시의 특징]((https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/01_data_structure.md#특징-5)
  2. [해시의 사용 예](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/01_data_structure.md#사용예-5)
  3. [java에서](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/01_data_structure.md#java에서-5)
  1. [충돌회피 방법]()
4. [Deque](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/01_data_structure.md#4-deque)
  1. [데크의 특징]((https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/01_data_structure.md#특징-6)
  2. [데크의 사용 예](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/01_data_structure.md#사용예-6)
  3. [java에서](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/01_data_structure.md#java에서-6)

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

<img src="https://github.com/HK-An/today_i_learned/blob/main/00_IMGS/01_COMPUTER_SCIENCE/time_complexity.png">

## Stack
<img src="https://github.com/HK-An/today_i_learned/blob/main/00_IMGS/01_COMPUTER_SCIENCE/stack.png">

> 마지막에 들어간 데이터가 가장 처음 나오는 자료구조 (LIFO; Last In First Out)

### 특징
1. 마지막에 들어간 자료가 가장 먼저 나온다. (후입선출, LIFO)
2. 자료의 최상위(top)에서만 접근할 수 있다.
3. 비어있는 스택에서 자료를 꺼내려고 하면 `Stack Underflow`, 스택이 넘칠 때는 `Stack Overflow`가 발생한다.
4. 속도
    - 삽입: O(1)
    - 삭제: O(1)
    - 탐색: O(n)

### 사용예
1. 재귀적 알고리즘
2. 후위 표기법 계산
3. 그래프의 [깊이 우선 탐색(DFS)](https://github.com/HK-An/today_i_learned/blob/main/04_ALGORITHM/DFS/definition.md)
4. 인터럽트처리, 수식의 계산, 서브루틴의 복귀 번지 저장 등

### Java에서
```java
import java.util.Stack;

public class Example{
  public void main() {
    Stack<Integer> stack = new Stack<>();
    stack.push(1); // 값 추가
    stack.push(2); // 값 추가
    stack.push(3); // 값 추가

    stack.pick(); // 3을 출력한다.(제거하지는 않는다.)
    stack.pop(); // 3을 출력한다. (stack에서 제거된다.)
    stack.clear(); // 스택의 전체 값 제거
    stack.empty(); // true; 스택이 비어있는지 확인
    stack.contains(1); // false; 스택에 해당 element가 있는지 확인
  }
}
```

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## Queue
<img src="https://github.com/HK-An/today_i_learned/blob/main/00_IMGS/01_COMPUTER_SCIENCE/queue.png">

> 가장 먼저 들어간 데이터가 먼저 나오는 자료구조 (FIFO; First In First Out)
### 특징
1. 데이터가 입력된 순서대로 처리가 이루어진다.  
2. 삭제연산이 이루어지는곳을 Front, 삽입연산이 이루어지는 곳을 Rear라고 한다.
3. 삭제연산을 디큐(deQueue), 삽입연산을 인큐(enQueue)라고 한다.

### 사용예
1. 프로세스 관리
2. 너비우선탐색(BFS)
3. 캐시(Cache)
4. 속도
    - 삽입: O(1)
    - 삭제: O(1)
    - 탐색: O(n)

### Java에서
```java
import java.util.Queue;
import java.util.LinkedList;

public class Example{
  public void main() {
    Queue<String> queue = new LinkedList<String>();
    queue.add(1); // 값 추가. 성공시 true 반환
    queue.add(2); // 값 추가. 실패시 IllegalStateException
    queue.offer(3); // 값 추가. 성공시 true 실패시 false 반환

    queue.peek(); // 1을 출력한다. (제거하지는 않는다.)
    queue.poll(); // 2(front 값)를 반환하고 제거함. queue가 비어있으면 null 반환
    queue.remove(); // 3을(front) 반환하고 제거
    queue.clear(); // 초기화
  }
}
```

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## Heap
<img src="https://github.com/HK-An/today_i_learned/blob/main/00_IMGS/01_COMPUTER_SCIENCE/heap.png">

> 힙은 최소값 혹은 최대값을 빠르게 찾기 위한 이진트리입니다. 최소 힙의 경우에는 부모가 자식보다 작고, 최대 힙의 경우에는 부모가 자식보다 큽니다. 힙의 삽입과 삭제는 O(logN)의 시간복잡도를 갖습니다.


최소값 및 최대값을 빠르게 찾아내기 위한 알고리즘(이진트리)이다.

### 특징
1. 완전이진트리를 기본 형태로 한다.
2. 특정 노드에 대한 서브트리(부모-자식)들도 조건을 만족한다.
3. 형제노드간에는 조건을 만족하지 않는다. (추가할때 마지막 노드에 추가하고 이에 따라 정렬하므로 벌어지는 현상, 반정렬상태)
4. Max-heap과 Min-heap의 두가지가 있다.
    - **Max-Heap**: 루트노드의 값이 자식노드들의 값보다 크거나 같은 트리.
    - **Min-Heap**: 루트노드의 값이 자식노드들의 값보다 작거나 같은 트리.
5. 속도
    - 삽입: O(logn) => 자료의 끝에 데이터를 추가하고 정렬한다.
    - 삭제: O(logn) => 삭제하고자 하는 노드와 최하위 노드를 바꾼다음에 재정렬한다.
    - 탐색: O(logn)
6. 배열을 사용하여 주로 구현한다. (편의를 위해 0번지는 비어있음)
7. 중복을 허용한다.

### 사용예
1. 네트워크 트래픽 제어
2. OS상의 작업 스케쥴링
3. 수치해석
4. 우선순위큐

### Java에서
```java
  public void minHeap() {
        PriorityQueue<Integer> queue = new PriorityQueue<>();
        queue.add(4);
        queue.add(0);
        queue.add(9);
        queue.add(2);
        queue.add(6);
        queue.add(1);

        for(int num : queue) {
            System.out.println(num); // 0, 2, 1, 4, 7, 9
        }

    }

    public void maxHeap() {
          PriorityQueue<Integer> queue = new PriorityQueue<>((o1, o2) -> Integer.compare(o2, o1));
          queue.add(4);
          queue.add(0);
          queue.add(9);
          queue.add(2);
          queue.add(6);
          queue.add(1);

          for(int num : queue) {
              System.out.println(num); // 9, 6, 4, 0, 2, 1
          }

      }
```

### 힙이 할 수 있는 것을 균형 이진 트리가 할 수 있지 않나?

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## 이진 탐색 트리
왼쪽 자식은 부모보다 작고 오른쪽 자식은 부모보다 큰 이진트리이다.

> 왼쪽 자식은 부모보다 작고 오른쪽 자식은 부모보다 큰 이진트리가 이진탐색트리입니다. 이진 탐색 트리는 삽입, 탐색, 삭제가 모두 트리의 높이인 O(logN ~ N)만큼의 시간복잡도를 갖습니다. 그래서 트리가 편향되게 하지 않기 위해 자가 균형트리를 사용합니다.

### 특징
1. 시간복잡도
삽입, 탐색, 삭제: O(logN ~ N)
### 사용예
### java에서

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## 자가 균형 트리
이진탐색트리에서 자료의 편향으로 인하여 효율성이 떨어지는것을 방지하기 위하여 삽입과 삭제를 개선한 이진트리이다.

> 이진탐색트리는 시간복잡도가 트리의 깊이에 의해 결정되므로 편향될경우 효율성이 떨어집니다. 그래서 편향되지 않게 삽입과 삭제를 개선한 이진탐색트리를 자가균형트리라고 합니다. 자가균형트리에는 AVL과 Red Black Tree가 있습니다.

### 특징
1. 시간복잡도
삽입, 탐색, 삭제: O(logN ~ N)

### 사용예
#### AVL
#### Red Black Tree

### java에서


[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## Hash
해시에 매핑하여 데이터를 저장하는 자료구조

> 해시는 해쉬에 매핑하여 데이터를 저장하는 자료구조입니다. Key는 hashFunction을 통해 hash로 변경된 다으멩 value와 매핑되어 bucket에 저장되게 됩니다. 시간복잡도는 삽입삭제조회가 모두 O(1)의 복잡도를 갖습니다.

### 특징
1. 시간복잡도
삽입, 탐색, 삭제: O(1)
2. 해시값을 도출하기 위한 해시함수는 동일한 데이터에 대한 항상 동일한 해시값을 리턴한다.
3. 같은 종류의 데이터를 묶어서 파악할 수 있다.
4. 기본적으로 하나의 해시값에 하나의 데이터를 지닌다.


### 사용예

### java에서

### 충돌회피 방법
> 충돌회피기법은 해시에서 하나의 버킷에 여러개의 데이터가 들어갈때 그 충돌을 회피하는 방법으로써 openAddresing chaining이 있습니다.openAddressing은 다른 해시값에 저장하는 방법이고 chainging은 해시 테이블에 원소 하나만을 담는게 아니라 likedList를 담는 방법입니다.    

- Open addressing  
 해시 충돌이 발생하면 다른 해시값에 저장하는 방법으로써 Linear Probing, Quadratic Probing, Double Hash 의 3가지 방법이 있다.

- Chainging  
<img src="https://github.com/HK-An/today_i_learned/blob/main/00_IMGS/01_COMPUTER_SCIENCE/hash_chaining.png">

해시 테이블에 하나의 원소를 담는게 아니라 linked list를 할당함으로써 데이터를 연결하여 해결한다. 수행시간이 빠르고, 메모리 낭비가 발생하지 않지만, 데이터 쏠림 현상이 발생할 수 있다.

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />


## Deque
<img src="https://github.com/HK-An/today_i_learned/blob/main/00_IMGS/01_COMPUTER_SCIENCE/deqye.jpg">

> Double Ended QUEue 데이터를 양방향으로 출입이 가능하도록 설계된 데이터 구조이다.

### 특징
### 사용예
### Java에서

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />
