# 기본 개념이 되는 내용들
## 목차
1. [자바의 특징](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/01_concept.md#%EC%9E%90%EB%B0%94%EC%9D%98-%ED%8A%B9%EC%A7%95)
2. [자바의 컴파일 과정](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/01_concept.md#%EC%9E%90%EB%B0%94%EC%9D%98-%EC%BB%B4%ED%8C%8C%EC%9D%BC-%EA%B3%BC%EC%A0%95)
3. [JVM의 구조](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/01_concept.md#jvm%EC%9D%98-%EA%B5%AC%EC%A1%B0)
4. [가비지 컬렉션의 동작흐름](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/01_concept.md#%EA%B0%80%EB%B9%84%EC%A7%80-%EC%BB%AC%EB%A0%89%EC%85%98%EC%9D%98-%EB%8F%99%EC%9E%91%ED%9D%90%EB%A6%84)
5. [클래스에 관하여](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/01_concept.md#%ED%81%B4%EB%9E%98%EC%8A%A4%EC%97%90-%EA%B4%80%ED%95%98%EC%97%AC)
6. [객체에 관하여](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/01_concept.md#%EA%B0%9D%EC%B2%B4%EC%97%90-%EA%B4%80%ED%95%98%EC%97%AC)
7. [캡슐화에 관하여](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/01_concept.md#%EC%BA%A1%EC%8A%90%ED%99%94%EC%97%90-%EA%B4%80%ED%95%98%EC%97%AC)
8. [상속에 관하여](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/01_concept.md#%EC%83%81%EC%86%8D%EC%97%90-%EA%B4%80%ED%95%98%EC%97%AC)
9. [다형성에 관하여](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/01_concept.md#%EB%8B%A4%ED%98%95%EC%84%B1%EC%97%90-%EA%B4%80%ED%95%98%EC%97%AC)
10. [스태틱에 관하여](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/01_concept.md#%EC%8A%A4%ED%83%9C%ED%8B%B1%EC%97%90-%EA%B4%80%ED%95%98%EC%97%AC)
11. [Final에 관하여](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/01_concept.md#final%EC%97%90-%EA%B4%80%ED%95%98%EC%97%AC)
12. [접근제어자에 관하여](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/01_concept.md#%EC%A0%91%EA%B7%BC%EC%A0%9C%EC%96%B4%EC%9E%90%EC%97%90-%EA%B4%80%ED%95%98%EC%97%AC)
13. [인터페이스 vs 추상클래스](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/01_concept.md#%EC%9D%B8%ED%84%B0%ED%8E%98%EC%9D%B4%EC%8A%A4-vs-%EC%B6%94%EC%83%81%ED%81%B4%EB%9E%98%EC%8A%A4)
14. [어노테이션에 관하여](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/01_concept.md#%EC%96%B4%EB%85%B8%ED%85%8C%EC%9D%B4%EC%85%98%EC%97%90-%EA%B4%80%ED%95%98%EC%97%AC)
15. [Overloding vs Overriding](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/01_concept.md#overloading-vs-overriding)
16. [스레드에 관하여](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/01_concept.md#%EC%8A%A4%EB%A0%88%EB%93%9C%EC%97%90-%EA%B4%80%ED%95%98%EC%97%AC)
17. [동기화 메소드에 관하여](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/01_concept.md#%EB%8F%99%EA%B8%B0%ED%99%94-%EB%A9%94%EC%86%8C%EB%93%9C%EC%97%90-%EA%B4%80%ED%95%98%EC%97%AC)
18. [직렬화에 관하여](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/01_concept.md#%EC%A7%81%EB%A0%AC%ED%99%94%EC%97%90-%EA%B4%80%ED%95%98%EC%97%AC)

## 자바의 특징
1. `이식성`이 높은 언어이다. (어떤 운영체제에서도 작동 가능하다.)
2. `객체 지향` 언어
3. `함수 스타일 코딩`을 지원한다.
4. `메모리를 자동으로 관리`한다. (해제해줄 필요가 없다.)
5. `멀티 스레드`를 쉽게 구현할 수 있다.
6. `동적 로딩`을 지원한다.  

> **동적로딩이란?**  
> 실행 시에 모든 클래스가 로딩되지 않고, 필요한 시점에 클래스를 로드하여 사용한다.
>
> **동적로딩의 장점**  
> 1. 일부 클래스가 변경되어도 전체 어플리케이션을 다시 컴파일하지 않아도 된다.
> 2. 변경사항이 발생해도 비교적 적은 작업만으로도 처리할 수 있는 유연한 어플리케이션을 작성할 수 있다.
> 3. 코드 블럭이 불연속적으로 위치하여도 된다.
> 4. 객체지향 개념이 적용 가능하도록 해준다.
>
> **동적로딩의 단점**
> 1. 실행 시 연결된 부분에 대한 판단을 해야하므로 속도 측면에서 불리하다.

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

7. `오픈소스가 풍부`하다.

## 자바의 `컴파일` 과정
1. 소스 파일(\*.java)을 `컴파일러(javac.exe)`로 컴파일하면 확장자가 `*.class`인 바이트 코드 파일이 생성된다.
2. 바이트 코드 파일은 `JVM 구동 명령어(java.exe)`에 의해 해석되고 해당 운영체제에 맞게 기계어로 번역된다.

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />


## JVM의 구조
### 1. Java Classloader
> 자바 클래스(\*.class) 파일을 자바 가상 머신으로 동적 로드하는 자바 런타임 환경(JRE)의 일부이다.

### 2. `JVM Memory(Runtime Data Area)`
> 클래스로더에 의해 데이터가 적재되는 공간

- `메소드 영역(Method Area)`: JVM이 시작할 때 생성되고 모든 스레드가 공유하는 영역으로 코드에서 사용되는 클래스들을 클래스로더로 읽어들여 **클래스별로 분류하고 저장**
- `힙 영역(Heap Area)`: **객체와 배열이 생성되는 영역**. JVM 스택 영역의 변수나 다른 객체의 필드에서 참조한다. 참조하는 변수나 필드가 없다면 의미가 없으므로 **Garbage Collector**가 미사용되는 쓰레기 객체를 힙 영역에서 자동으로 제거한다.
- `JVM Stack`: **각 스레드마다 하나 존재하며 스레드가 시작될 때 할당**된다. 메소드를 호출할 때마다 프레임을 추가(push)하고 메소드가 종료되면 해당 프레임을 제거(pop)하는 동작을 수행한다. 프레임 내부에는 `로컬 변수 스택`이 존재할 수 있다.
- `PC Registers`: 실행할 명령의 주소를 가지고 있음
- `Native Method Stacks`: 스레드에서 네이티브 방식의 메소드가 실행되면 해당 스택에 쌓인다.

### 3. Execution Engine
> 클래스로더에 의해 JVM 메모리 공간에 적재된 바이트 코드를 실행하기 전에 기계어로 변경 후 사용한다.

변경 방법에는 인터프리터(Interpreter)와 JIT(Just-In-Time) compiler가 있다.

### 4. Native Method Interface
자바 가상 머신 위에서 실행되고 있는 자바 코드가 네이티브 응용 프로그램(하드웨어와 운영 체제 플랫폼에 종속된 프로그램들)과 다른 언어들로 작성된 라이브러리들을 호출하거나 반대로 호출되는 것을 가능하게 하는 프로그래밍 프레임워크

### 5. Native Method Library

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />


## `가비지 컬렉션`의 동작흐름
> GC(Garbage Collector)라고 불리는 데몬 스레드에 의하여 실행되며 대상이 되는 객체를 힙에서 제거

1. 객체를 제거하기 전 해당 객체의 `finalize()` 메소드를 호출한다.
2. GC는 **강제로 수행될 수 없으며**, JVM이 힙 사이즈에 기반하여 필요한 경우에만 수행한다.
3. System.gc()와 Runtime.gc()는 GC를 실행시키는 동작이 아닌, 권유하는 기능이므로 수행이 보장되지 않는다.
4. 힙에 새로운 객체를 생성할 메모리가 없다면, **Out of Memory** 에러를 출력한다.

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## `클래스`에 관하여
> 자바의 클래스는 설계도와 같다.

- 클래스로부터 새로운 객체를 생성하는 것을 **인스턴스화**라고 한다.
- 클래스로부터 생성된 새로운 객체를 **인스턴스**라고 한다.

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## `객체`에 관하여
> 물리적으로 존재하거나 추상적으로 존재하는 것 , 속성을 가지고 있고 다른것과 구별할 수 있는 것

- 객체는 속성과 동작으로 구분되어 있는데, 이를 **필드**와 **메소드**라고 부른다.
- 현실 세계의 객체를 소프트웨어의 객체로 설계하는 것을 **모델링**이라고 부른다.

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## `캡슐화`에 관하여
> 객체의 필드나 메소드를 외부에서 접근하지 못하도록 구현 내용을 감추는 것

- 외부의 잘못된 사용으로 해당 객체의 무결성이 깨지는 것을 방지한다.
- 자바에서는 접근 제한자를 통하여 구현 가능하다.

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## `상속`에 관하여
> 부모가 가지고 있는 성질을 자식에게 물려주는 것

상속을 통하여 기대할수 있는것은 아래와 같다.  
1. 상위 객체를 재사용하여 하위 객체를 **쉽고 빠르게 설계**할 수 있다.
2. 반복되는 **코드의 중복을 제거**한다.
3. **코드의 개발 시간을 단축**할 수 있다.
4. **유지보수에 들어가는 비용을 절약**할 수 있다.

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## `다형성`에 관하여
> 같은 타입이지만 다른 결과를 가지는 객체를 이용할 수 있는 성질

하나의 타입에 여러  객체를 대입함으로 다양한 기능을 이용할 수 있게 해주며 부모 객체에는 모든 자식 객체가, 인터페이스 객체에는 모든 구현 객체가 도입될 수 있다.

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## `스태틱`에 관하여
> static은 `정적`이라는 의미로 메모리 할당을 1회만 수행한다.

같은 메모리 주소를 바라보므로 값을 공유하며, 주로 메모리 효율성적인 측면보다는 해당 데이터를 공유하기 위한 목적으로 많이 사용한다.  
메소드에 static이 붙을 시에는 해당 메소드 안에서는 인스턴스 변수 접근이 불가능하며, static 변수만이 static 메소드에 접근할 수 있다.

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## `Final`에 관하여
- final class: 다른 클래스에서 상속하지 못한다.
- final method: 다른 메소드에서 오버라이딩하지 못한다.
- final variable: 변하지 않는 상수가 되어 새로 할당할 수 없는 변수가 된다.

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## `접근제어자`에 관하여
|접근제한|적용대상|접근할 수 없는 클래스|
|-|-|-|
|public|클래스,필드,생성자,메소드|없음|
|protected|필드,생성자,메소드|자식 클래스가 아닌 다른 패키지에 속한 클래스|
|default|클래스,필드,생성자,메소드|다른 패키지에 속한 클래스|
|private|필드,생성자,메소드|모든 외부 클래스|

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## `인터페이스` vs `추상클래스`
- [인터페이스](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/concept/interface/definition.md)
> 구현 객체와 같은 동작을 보장하기 위하여 사용

    - 클래스가 아니다
    - 한 개의 클래스에 여러 인터페이스를 구현할 수 있다.
    - 동일한 기능을 구현하게끔 메소드를 추상적으로 미리 정의하여 다형성을 극대화시킴

- [추상클래스](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/concept/abstract_class/definition.md)
> 상속을 강제하여 기능을 확장하기 위하여 사용

    - 인터페이스와 다르게 자체가 클래스이다.
    - 한 개의 클래스에 한 개의 추상 클래스만을 사용할 수 있다.
    - 코드에 반복되는 내용이  있을 시에 이것을 미리 구현하여 개발자가 상황에 따라 구현없이도 사용할 수 있게끔 한다.

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## `어노테이션`에 관하여
> 일종의 메타데이터로 컴파일 과정과 실행 과정에서 코드를 어떻게 컴파일하고 처리할 것인지 알려주는 정보

어노테이션 그 자체로는 주석에 가까운 표식이지만, 리플렉션을 이용해 어노테이션 적용 여부와 엘리먼트 값을 읽고 처리할 수 있다. 어노테이션 제공의 목적은 아래와 같다.
1. 컴파일에게 코드 문법 에러를 체크하도록 정보를 제공
2. 소프트웨어 개발 툴이 빌드나 배치시 코드를 자동으로 생성할 수 있도록 정보를 제공
3. 실행 시(런타임시) 특정 기능을 실행하도 정보를 제공

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## `Overloading` vs `Overriding`
- [Overloading](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/concept/overloading/definition.md)  
오버로딩은 객체 지향 프로그래밍에서 다형성에 의하여 같은 이름을 가진 메소드를 연산자를 다르게 하여 여러번 재정의해서 사용하는 것을 의미한다.

- [Overriding](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/concept/overriding/definition.md)  
객체지향 프로그래밍에서 자식 클래스가 자신의 부모 클래스들 중 하나에 이미 정의된 메소드를 재정의하는 기술이다.

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## `스레드`에 관하여
> 일반 스레드와 큰 차이가 없으며, 자바 가상 머신이 운영체제의 역할을 함

자바 스레드는 JVM에 의하여 스케쥴되는 실행 단위 코드 블록이다.(자바에는 프로세스가 존재하지 않는다.)

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## `동기화 메소드`에 관하여
> 동기화 메소드는 한 스레드가 작업 중인 객체에 다른 스레드가 접근할 수 없도록 잠금을 걸어두는 기능(동기화)을 제공하는 메소드

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## [`직렬화`](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/concept/serialize_definition.md)에 관하여
> 자바 시스템 내부에서 사용되는 객체 또는 데이터를 외부의 자바 시스템에서도 사용할 수 있도록 바이트 형태로 데이터 변환하는 기술과 바이트로 변환된 데이터를 다시 객체로 변환하는 기술

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />
