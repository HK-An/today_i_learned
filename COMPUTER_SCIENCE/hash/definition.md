# Hash (해시)

## 개요
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/5/58/Hash_table_4_1_1_0_0_1_0_LL.svg/240px-Hash_table_4_1_1_0_0_1_0_LL.svg.png">  

자료 구조에서의 해시는 특정 데이터에 대하여 데이터를 저장하기 위한 색인(Index)에 해시 함수를 통하여 특정 해시값을 구하여 저장하거나 탐색하는 자료 구조를 말한다.

## 특징
1. 해시값을 도출하기 위한 해시함수는 동일한 데이터에 대한 항상 동일한 해시값을 리턴한다.
2. 같은 종류의 데이터를 묶어서 파악할 수 있다.
3. 기본적으로 하나의 해시값에 하나의 데이터를 지닌다.

## 장점
1. 데이터를 삽입, 수정, 삭제하는데 걸리는 시간복잡도가 적다. `O(1)`
2. 알고리즘이 비교적 복잡하지 않아, 해당 알고리즘에 들어가는 리소스가 비교적 적다.

## 단점
1. 해시충돌(각자 다른 데이터가 같은 해시값을 가짐)이 발생할 수 있다.
2. 순서/관계가 있는 데이터의 경우에는 효율적이지 않을 수도 있다.
3. 해시함수에 대한 의존도가 높기 때문에, 해시 함수가 복잡한 경우, 해시값을 만들어내는데에 시간이 오래걸릴 수도 있다.

## 해시 충돌이 발생할 경우
### 1. Chaining
<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FnMfgg%2FbtqS1WyRuWI%2F32LmJGOvrT9YTndHMvYW50%2Fimg.png">
해시 충돌이 발생한 경우, 해당 해시값에 연결리스트를 할당함으로써 데이터를 연결하여 해결한다. 수행시간이 빠르고, 메모리 낭비가 발생하지 않지만, 데이터 쏠림 현상이 발생할 수 있다.

### 2. Open Addressing
#### 2.1. Linear Probing
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/90/HASHTB12.svg/362px-HASHTB12.svg.png">

해시충돌이 발생한 경우 바로 다음 주솟값에 삽입하는 방법이다. 만약, 다음 주소에도 데이터가 있으면 그 다음 주소에 데이터를 입력한다.
이 방법은 특정 영역에 데이터가 몰릴 가능성이 있으며, 이는 충돌의 확률을 높이는 결과를 초래한다.

#### 2.2. Quadratic Probing
<img src="https://www.codingeek.com/wp-content/uploads/2017/07/linear-and-quadratic-probing-300x173.png" width=1000px>

Linear Probing이 바로 다음 주솟값에 삽입하는 방법이면, Quadratic Probing은 해당 주솟값이 사용중이면 주솟값에 n^2한 주솟값의 옆 칸을 검토하는 방법이다. 예를 들면 다음과 같다.
> 1^2+1(2) => 2^2+1(5) => 5^2+1(26) => 25^2+1(626) => ...  

#### 3. Double Hash
해시 연산을 2번하여 해시 충돌을 피하는 방법으로써, "해쉬 값이 같으면 충돌 발생시 빈 슬롯을 찾기 위해 접근하는 위치가 늘 동일하다"라는 문제점에서 착안한 방법이다.  
1차 해시함수는 기존 방법과 같이 키를 근거로 주솟값을 연산하며,  
2차 해시함수는 해시충돌 발생시 몇칸 뒤를 살필지 결정한다.
