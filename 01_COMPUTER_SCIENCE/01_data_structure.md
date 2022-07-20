# 자료구조
## 목차
1. [Stack](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/01_data_structure.md#1-stack)
    1. [스택의 특징](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/01_data_structure.md#%ED%8A%B9%EC%A7%95)
    2. [스택의 사용 예](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/01_data_structure.md#%EC%82%AC%EC%9A%A9%EC%98%88)
    3. [java에서](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/01_data_structure.md#java%EC%97%90%EC%84%9C)
2. [Queue](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/01_data_structure.md#2-queue)
    1. [큐의 특징](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/01_data_structure.md#%ED%8A%B9%EC%A7%95-1)
    2. [큐의 사용 예](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/01_data_structure.md#%EC%82%AC%EC%9A%A9%EC%98%88-1)
    3. [java에서](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/01_data_structure.md#java%EC%97%90%EC%84%9C-1)
3. [Heap](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/01_data_structure.md#3-heap)
    1. [힙의 특징](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/01_data_structure.md#특징-2)
    2. [힙의 사용 예](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/01_data_structure.md#%EC%82%AC%EC%9A%A9%EC%98%88-2)
    3. [java에서](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/01_data_structure.md#java%EC%97%90%EC%84%9C-2)

<hr />

### 1. Stack
<img src="https://github.com/HK-An/today_i_learned/blob/main/00_IMGS/01_COMPUTER_SCIENCE/stack.png">

> 마지막에 들어간 데이터가 가장 처음 나오는 자료구조 (LIFO; Last In First Out)
#### 특징
1. 마지막에 들어간 자료가 가장 먼저 나온다. (후입선출, LIFO)
2. 자료의 최상위(top)에서만 접근할 수 있다.
3. 비어있는 스택에서 자료를 꺼내려고 하면 `Stack Underflow`, 스택이 넘칠 때는 `Stack Overflow`가 발생한다.

#### 사용예
1. 재귀적 알고리즘
2. 후위 표기법 계산
3. 그래프의 [깊이 우선 탐색(DFS)](https://github.com/HK-An/today_i_learned/blob/main/04_ALGORITHM/DFS/definition.md)
4. 인터럽트처리, 수식의 계산, 서브루틴의 복귀 번지 저장 등

#### Java에서
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

### 2. Queue
<img src="https://github.com/HK-An/today_i_learned/blob/main/00_IMGS/01_COMPUTER_SCIENCE/queue.png">

> 가장 먼저 들어간 데이터가 먼저 나오는 자료구조 (FIFO; First In First Out)
#### 특징
1. 데이터가 입력된 순서대로 처리가 이루어진다.  
2. 삭제연산이 이루어지는곳을 Front, 삽입연산이 이루어지는 곳을 Rear라고 한다.
3. 삭제연산을 디큐(deQueue), 삽입연산을 인큐(enQueue)라고 한다.

#### 사용예
1. 프로세스 관리
2. 너비우선탐색(BFS)
3. 캐시(Cache)

#### Java에서
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

## 3. Heap
<img src="https://github.com/HK-An/today_i_learned/blob/main/00_IMGS/01_COMPUTER_SCIENCE/heap.png">

> 최소값 및 최대값을 빠르게 찾아내기 위한 알고리즘.

### 특징
1. 완전이진트리를 기본 형태로 한다.
2. 특정 노드에 대한 서브트리(부모-자식)들도 조건을 만족한다.
3. 형제노드간에는 조건을 만족하지 않는다. (추가할때 마지막 노드에 추가하고 이에 따라 정렬하므로 벌어지는 현상, 반정렬상태)
4. Max-heap과 Min-heap의 두가지가 있다.
    - **Max-Heap**: 루트노드의 값이 자식노드들의 값보다 크거나 같은 트리.
    - **Min-Heap**: 루트노드의 값이 자식노드들의 값보다 작거나 같은 트리.
5. 속도
    - 삽입: O(logn)
    - 삭제: O(logn)
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
