# 자바의 데이터 타입 및 기타 타입들

## 목차
1. [기본 데이터 타입](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/02_type.md#기본-데이터-타입)
2. [`제네릭`타입](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/02_type.md#제네릭타입)
3. [`String`, `StringBuffer`, `StringBuilder`의 차이](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/02_type.md#string-stringbuffer-stringbuilder의-차이)
4. [`List`에 관하여](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/02_type.md#list에-관하여)
5. [`Set`에 관하여](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/02_type.md#set에-관하여)
6. [`Map`에 관하여](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/02_type.md#map에-관하여)

## 기본 데이터 타입
> 정수, 실수, 문자, 논리 리터럴을 직접 저장하는 타입

|값의 종류|기본 타입|메모리 사용 크기|
|-|-|-|
|정수|byte|1byte, 8bit|
|정수|char|2byte, 16bit|
|정수|short|2byte, 16bit|
|정수|int|4byte, 32bit|
|정수|long|8byte, 64bit|
|실수|float|4byte, 32bit|
|실수|double|8byte, 64bit|
|논리|boolean|1byte, 8bit|

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## `제네릭`타입
> 잘못된 타입이 사용될 수 있는 문제를 컴파일 과정에서 제거할 수 있게 하는 것

클래스와 인터페이스, 메소드를 정의할 때 타입을 파라미터로 사용할 수 있도록 한다. 그로 인해 컴파일 시 강한 타입 체크를 하여 런타입에 발생하는 타입 에러를 미연에 방지한다.  
또한 타입 변환을 제거한다. 비제너릭 코드는 불필요한 타입 변환을 하기 때문에 프로그램 성능에 악영향을 미치는 경우도 있는데, 이러한 경우를 방지한다.

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## `String`, `StringBuffer`, `StringBuilder`의 차이
### String
> 문자열을 저장하며 내부 문자열의 수정이 불가능함

- `replace()` 메서드의 경우 내부 문자를 대체하는 것이 아니라 해당 문자열을 대체한 새로운 String 객체를 생성하여 return 하는 것이다.
- 문자열을 결합하는 `+`도 많이 사용하면 String 객체의 수가 늘어나 성능 저하가 발생할 수 있으므로, 문자열 변경이 많으면 `StringBuffer` 또는 `StringBuilder` 클래스를 권장한다.

### StringBuffer, StringBuilder
> 문자열을 수정하면서 메모리가 부족할 경우 자동으로 버퍼 크기를 늘림

- 해당 클래스들은 내부 버퍼에 문자열을 저장하여 필요시 버퍼의 크기를 유동적으로 조정한다.
- 두 클래스의 사용법은 동일하지만 스레드 환경에서의 차이가 존재한다.
    - `StringBuffer`: 멀티 스레드 환경에서 사용할 수 있도록 동기화가 적용되어 있어 스레드에 안전하다.
    - `StringBuilder`: 단일 스레드 환경에서만 사용하도록 설계되어 있다.

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## `List`에 관하여
> List는 순서를 유지하고 중복 저장이 가능함

구현 클래스는 아래의 3가지가 있다.
1. ArrayList  
메모리 내에서 연속적인 주솟값을 가진다. 기본적으로 동기화되어있지 않기 때문에 경우에따라 동기화처리 필요하다.
2. Vector  
ArrayList의 전신. ArrayList와 거의 비슷한 기능을 한다. 하지만 기본적으로 동기화되어 thread-safe하다. 하지만 동시에 ArrayList에 비해 성능이 떨어진다.
3. LinkedList  
메모리 내에서 불연속적인 주소를 가지며, 현재 노드는 다음 노드의 주소를 가리킨다.

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## `Set`에 관하여
> Set은 순서를 유지하지 않고 중복 저장이 불가능함

구현 클래스는 아래의 2가지가 있다.
1. HashSet  
기본적인 `Set`인터페이스의 특징대로 순서를 유지하지 않고 중복 저장이 불가능하다. 하지만 인스턴스가 다른 경우 다른 값으로 인식하는 경우가 있기 때문에 이 경우에는 `equals()`와 `hashCode()`를 오버라이딩하여 수정하여 사용하여야 한다.
2. TreeSet(SortedSet)  
[레드-블랙 트리]()의 형태로 데이터를 저장한다. 그러므로 `Set`의 특성처럼 저장순서를 유지하지 않지만, 자동으로 정렬된 위치에 데이터를 저장한다. 이로인해, 추가와 삭제에는 시간이 조금 더 걸리지만 검색과 정렬에는 시간적으로 유리하다.

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## `Map`에 관하여
> Map은 키와 값의 쌍으로 저장되며, 키를 중복으로 저장할 수 없음

구현 클래스는 아래의 4가지가 있다.
1. HashMap  
`Map` 인터페이스의 일반적인 특징을 지닌다. 기본적으로는 동기화되어있지 않으며, 동기화를 위해서는 처리가 별도로 필요하다.
2. HashTable  
최초의 해시 테이블을 구현한 자료형으로, HashMap의 전신이며 `Map`인터페이스의 일반적인 특징을 지닌다. 기본적으로 동기화되어 thread-safe하다. 하지만 동시에 HashMap에 비해 성능이 떨어진다.
3. TreeMap(SortedMap)  
[레드-블랙 트리]()의 형태로 키를 정렬하여 저장한다. 데이터 저장시, 자동으로 정렬이 이루어져 추가나 삭제가 `HashMap`에 비해 떨어지지만, 정렬된 데이터를 조회할 시 효율성면에서 유리하다.
4. Properties  
`HashTable`을 상속받아 모든 특징을 그대로 가지고 있다. 하지만 키와 값을 String만 사용할 수 있다.

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />
