# 기본 개념이 되는 내용들
## 목차
1. [자바의 특징](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/01_concept.md#자바의특징)
  1. [동적로딩](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/01_concept.md#동적로딩)
2. [객체지향](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/01_concept.md#객체지향)
  1. [객체](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/01_concept.md#객체)
  5. [클래스](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/01_concept.md#클래스)
  1. [객체지향 프로그래밍의 4가지 특징](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/01_concept.md#객체지향-프로그래밍의-4가지-특징)  
      1. [추상화](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/01_concept.md#추상화)  
      1. [캡슐화](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/01_concept.md#캡슐화)
      1. [상속성](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/01_concept.md#상속성)
      1. [다형성](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/01_concept.md#다형성)
  1. [객체지향 설계 5대 원칙](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/01_concept.md#객체지향-설계-5대-원칙)
  13. [인터페이스와 추상클래스](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/01_concept.md#인터페이스와-추상클래스)
  1. [객체지향, 함수형의 차이](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/01_concept.md#객체지향-함수형의-차이)
  15. [Overloding과 Overriding](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/01_concept.md#overloading과-overriding)
2. [자바 실행 과정](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/01_concept.md#자바-실행-과정)
3. [JVM의 구조](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/01_concept.md#jvm의-구조)
  1. [클래스 로드 방법](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/01_concept.md#클래스-로드-방법)
  1. [클래스 로드 과정](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/01_concept.md#클래스-로드-과정)
1. [자바메모리구조](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/01_concept.md#자바메모리구조)
   1. [스레드별로 부여되는 영역](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/01_concept.md#스레드별로-부여되는-영역)
   1. [공통으로 사용하는 영역](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/01_concept.md#공통으로-사용하는-영역)
4. [가비지 컬렉션](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/01_concept.md#가비지-컬렉션)
  1. [가비지 컬렉션 일어나는 과정](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/01_concept.md#가비지-컬렉션이-일어나는-과정)
  1. [GC 모니터링](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/01_concept.md#GC-모니터링)
1. [Servlet](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/01_concept.md#servlet)
  1. [개념](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/01_concept.md#개념)
  1. [동작순서](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/01_concept.md#동작순서)
  1. [생명주기](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/01_concept.md#생명주기)
1. [변수](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/01_concept.md#변수)
  1. [정적변수](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/01_concept.md#정적변수)
  2. [전역변수](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/01_concept.md#전역변수)
12. [접근제어자](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/01_concept.md#%접근제어자)
18. [직렬화](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/01_concept.md#직렬화)
  1. [SerialVersionUID](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/01_concept.md#serialversionuid)
1. [Wrapper Class](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/01_concept.md#wrapper-class)
  1. [String은 래퍼클래스인데 == 비교시 값 같게 나오는 이유](
1. [제네릭](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/01_concept.md#제너릭)
11. [Final](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/01_concept.md#final)
1. [자바 버전](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/01_concept.md#자바버전)
10. [Static](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/01_concept.md#static)
14. [Annotation](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/01_concept.md#annotation)
17. [동기화 메소드](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/01_concept.md#동기화-메소드)

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## 자바의 특징
1. 이식성이 높은 언어이다. (어떤 운영체제에서도 작동 가능하다.)
2. 객체 지향 언어
3. 함수 스타일 코딩을 지원한다.
4. 메모리를 자동으로 관리한다. (해제해줄 필요가 없다.)
5. 멀티 스레드를 쉽게 구현할 수 있다.
6. 동적 로딩을 지원한다.  
7. 오픈소스가 풍부하다.

> 자바의 특징은 총 일곱가지가 있습니다. 첫째로 이식성이 높은 언어라는 점이고, 둘째 객체지향 언어입니다. 셋째, 람다식으로 함수 스타일 코딩을 지원하며, 넷째, 가비지컬렉터로 메모리를 자동으로 관리해줍니다. 다섯번째로 멀티 스레드를 쉽게 구현할 수 있으며, 여섯번째로 동적 로딩을 지원합니다. 마지막 일곱번째로 오픈소스가 풍부하다는 점이 있습니다.

### 동적로딩  
 실행 시에 모든 클래스가 로딩되지 않고, 필요한 시점에 클래스를 로드하여 사용한다.

#### 장점  
1. 일부 클래스가 변경되어도 전체 어플리케이션을 다시 컴파일하지 않아도 된다.
2. 변경사항이 발생해도 비교적 적은 작업만으로도 처리할 수 있는 유연한 어플리케이션을 작성할 수 있다.
3. 코드 블럭이 불연속적으로 위치하여도 된다.
4. 객체지향 개념이 적용 가능하도록 해준다.

#### 단점
1. 실행 시 연결된 부분에 대한 판단을 해야하므로 속도 측면에서 불리하다.

> 동적로딩은 실행 시에 모든 클래스가 로딩되지 않고 필요한 시점에 필요한 클래스를 로드하는 것으로써 객체지향 개념이 가능하도록 해줍니다. 하지만 연결 부분에 대한 판단으로 인하여 속도 측면에서는 불리하다라는 단점을 가지고 있습니다.

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## 객체지향
현실 세계의 사물같은 객체를 만들고 객체에서 필요한 특징을 뽑아서 프로그래밍을 수행하는 것.

### 객체
물리적으로 존재하거나 추상적으로 존재하는 것, 속성을 가지고 있고 다른것과 구별할 수 있는 것을 의미한다.

### 클래스
자바의 클래스는 설계도와 같다.클래스로부터 새로운 객체를 생성하는 것을 인스턴스화라고 하고, 클래스로부터 생성된 새로운 객체를 인스턴스라고 한다.

### 객체지향 프로그래밍의 4가지 특징
#### 추상화
객체화 시키는 사물의 특징을 뽑아서 공통적인 요소를 가지는 하나의 클래스로 만드는 것을 의미한다.
#### 캡슐화
정보은닉을 통해서 높은 내부 응집도를 가지고 낮은 외부 결합도를 가지는 것을 의미한다.
#### 상속성
기존 클래스에서 공통된 내용을 뽑아 그대로 상속받아서 새로운 내용을 추가하여 사용할수 있게 하는 것을 의미한다.
#### 다형성
하나의 클래스가 여러가지 타입을 가질 수 있는 것을 의미한다.
> 현실 세계의 사물과 같은 객체를 만들고 그 객체에서 필요한 특징을 뽑아서 프로그래밍을 수행하는 것입니다. 객체지향 프로그래밍은 총 4가지 특징이 있는데 추상화, 캡슐화, 상속성, 다형성이 있습니다. 추상화는 공통적인 특성을 뽑아내 객체화 시키는 것을 의미하고 캡슐화는 정보은닉을 통하여 높은 응집도와 낮은 결합도를 가지는 것입니다. 상속성은 기존에 있는 클래스에서 공통된 내용을 뽑아 재사용할 수 있는 것을 의미하며 다형성은 하나의 클래스가 여러 타입을 가질 수 있는 것을 의미합니다.

### 객체지향 설계 5대 원칙
- **단일 책임 원칙**  
모든 클래스는 하나의 기능만을 가진다.

- **개방 폐쇄 원칙**  
소프트웨어의 클래스, 모듈, 함수 등은 확장에는 열려있고, 변경에는 닫혀있어야 한다.

- **리스코프 치환 원칙**  
부모 클래스를 상속받은 자식 클래스는 부모 클래스의 역할을 할 수 있어야 한다.

- **인터페이스 분리 원칙**  
자신이 사용하지 않는 인터페이스는 사용하면 안된다.

- **의존관계 역전 원칙**  
상위 모율은 하위 모듈에 의존해서는 안된다.

### 인터페이스와 추상클래스
#### 인터페이스
interface 지시자로 정의되며 구현 객체와 같은 동작을 보장하기 위하여 사용한다. 모든 메소드를 추상메소드로 정의하여야 하며, 보장을 목적으로 사용한다.
#### 추상클래스
abstract 지시자로 정의되며 상속을 강제하여 기능을 확장하기 위하여 사용하며 추상메소드가 하나이상 포함된다. 상속에 대한 목적으로 사용된다.

> 추상클래스는 abstract로 지시자로 정의되어서 추상메소드가 하나 이상 포함되는 클래스이구요 인터페이스는 interface 지시자로 정의되어서 모든 메소드가 추상메소드로 정의되게 됩니다. 추상클래스와 인터페이스의 차이는 그 존재의 목적에 있습니다. 추상 클래스는 상속받아서 기능을 재활용하고 확장시키는데 목적이 있다고 하면, 인터페이스는 함수의 구현을 강제해서 구현한 객체들이 같은 동작을 하는것을 보장하는 것에 목적이 있습니다.

### 객체지향, 함수형의 차이

### Overloading과 Overriding
#### Overloding
오버로딩은 객체 지향 프로그래밍에서 다형성에 의하여 같은 이름을 가진 메소드를 연산자를 다르게 하여 여러번 재정의해서 사용하는 것을 의미한다.
#### Overriding
객체지향 프로그래밍에서 자식 클래스가 자신의 부모 클래스들 중 하나에 이미 정의된 메소드를 재정의하는 기술이다.

> 오버로딩은 다형성에 입각하여 같은 이름을 가진 메소드를 인수 등을 다르게 하여 재정의 하는 방법이고, 오버라이딩은 부모 클래스에 이미 정의된 메소드를 부모 클래스를 상속받은 자식 클래스가 재정의하는 기술입니다.


[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## 자바 실행 과정

<img src="https://github.com/HK-An/today_i_learned/blob/main/00_IMGS/02_JAVA/java_compiler.jpg">

1. 소스 파일(\*.java)을 컴파일러(javac.exe)로 컴파일하면 확장자가 *.class인 바이트 코드 파일이 생성된다.
2. 바이트 코드 파일은 JVM 구동 명령어(java.exe)에 의해 해석되고 해당 운영체제에 맞게 기계어로 번역된다.

> 컴파일러가 자바 소스를 바이트코드로 변환합니다. 클래스로더가 바이트 코드를 런타임 데이터 영역에 로드시키구요. 로딩된 바이트 코드가 실행엔진에 의해서 실행되게 됩니다.

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## JVM의 구조

<img src="https://github.com/HK-An/today_i_learned/blob/main/00_IMGS/02_JAVA/jvm.png">

### 클래스 로드 방법


### 클래스 로드 과정
1. 메소드 호출하는 문장을 만났는데, 해당하는 클래스 바이트코드가 로드된적이 없다면 JVM은 JRE 라이브러리 폴더에서 클래스를 찾는다.
2. JRE 라이브러리에 없으면 CLASSPATH 환경변수에 지정된 폴더에서 클래스를 찾는다.
3. 찾은 클래스를 올바른지 판단하기 위하여 바이트코드를 검증한다.
4. 올바른 바이트코드일 경우 메소드영역으로 로드한다.
5. 클래스 변수를 만들어야 할 경우, 메소드 영역에 변수를 준비한다.
1. 클래스 블록이 있으면 순서대로 블록을 실행한다.
1. 클래스의 바이트코드는 JVM이 종료될때까지 유지된다.
### Java Classloader
자바 클래스(\*.class) 파일을 자바 가상 머신으로 동적 로드하는 자바 런타임 환경(JRE)의 일부이다.

### Execution Engine
클래스로더에 의해 JVM 메모리 공간에 적재된 바이트 코드를 실행하기 전에 기계어로 변경 후 사용한다. 방법에는 인터프리터(Interpreter)와 JIT(Just-In-Time) compiler가 있다.
### Native Method Interface
자바 가상 머신 위에서 실행되고 있는 자바 코드가 네이티브 응용 프로그램(하드웨어와 운영 체제 플랫폼에 종속된 프로그램들)과 다른 언어들로 작성된 라이브러리들을 호출하거나 반대로 호출되는 것을 가능하게 하는 프로그래밍 프레임워크
### Native Method Library

## 자바메모리구조
클래스로더에 의해 데이터가 적재되는 공간이다.

#### 스레드별로 부여되는 영억
- **PC Register**  
실행할 명령의 주소를 저장한다.
- **JVM Stack**  
메소드에 대한 정보를 저장한다.
- **Native Method Stack**  
자바외의 네이티브 방식의 메소드를 수행하기 위해 존재하는 공간이다.
#### 공통으로 사용하는 영역
- **메소드 영역**  
코드에서 사용되는 클래스들을 클래스로더로 읽어들여 클래스별로 분류하고 저장하는 공간이다.
- **힙 영역**  
개발자가 사용하는 공간으로써 변수 등이 저장되는 공간이다.

> 자바 메모리 구조는 크게 5가지 영역으로 구분되는데요 우선 스레드마다 PC Register, JVM Stack, 그리고 Native Method Stack 이 있고
Thread 공통으로는 Heap과 Method Area가 있습니다. PC Register는 현재 수행중인 JVM 명령어가 들어가있구요 JVM Stack은 호출된 메소드의 매개변수, 지역변수, 리턴정보들이 저장됩니다. Native Method Stack은 자바 외의 언어인 C나 C++ 같은 것들을 수행하기 위한 영역이구요 Method Area는 클래스 별로 전역변수, 정적변수, 메소드 정보들이 저장되게 됩니다. 마지막으로 Heap영역은 런타임중 생성되는 객체들이 동적으로 할당되는 곳입니다.

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## 가비지 컬렉션
GC(Garbage Collector)라고 불리는 데몬 스레드에 의하여 실행되며 대상이 되는 객체를 힙에서 제거한다.

### 가비지 컬렉션이 일어나는 과정
1. 객체를 제거하기 전 해당 객체의 finalize() 메소드를 호출한다.
2. GC는 강제로 수행될 수 없으며, JVM이 힙 사이즈에 기반하여 필요한 경우에만 수행한다.
3. System.gc()와 Runtime.gc()는 GC를 실행시키는 동작이 아닌, 권유하는 기능이므로 수행이 보장되지 않는다.
4. 힙에 새로운 객체를 생성할 메모리가 없다면, `Out of Memory` 에러를 출력한다.

### GC 모니터링

> gc는 jvm에서 메모리를 관리해주는 모듈입니다. heap 메모리를 재활용하기 위해서 더이상 참조되지 않는 객체들을 메모리에서 제거하는 모듈입니다. 개발자가 직접 메모리를 정리하지 않아도 되어서 개발속도가 향상되는 장점이 있지만 Mark and Sweep이라는 과정에서 참조되지 않는 객체를 찾는 과정이 있는데, 이때 스레드가 잠깐 중단되어서  성능이 떨어진다는 단점이 있습니다.

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## Servlet
### 개념
자바 서블릿은 자바를 사용하여 웹페이지를 동적으로 생성하는 서버측 프로그램 혹은 그 사양을 말하며, 흔히 "서블릿"이라 불린다. 자바 서블릿은 웹 서버의 성능을 향상하기 위해 사용되는 자바 클래스의 일종이다. 서블릿은 JSP와 비슷한 점이 있지만, JSP가 HTML 문서 안에 Java 코드를 포함하고 있는 반면, 서블릿은 자바 코드 안에 HTML을 포함하고 있다는 차이점이 있다.

### 동작순서
<img src="https://github.com/HK-An/today_i_learned/blob/main/00_IMGS/02_JAVA/servlet.png">
1. 사용자(클라이언트)가 URL을 입력하면 HTTP Request가 Servlet Container로 전송합니다.
2. 요청을 전송받은 Servlet Container는 HttpServletRequest, HttpServletResponse 객체를 생성합니다.
3. web.xml을 기반으로 사용자가 요청한 URL이 어느 서블릿에 대한 요청인지 찾습니다.해당 서블릿에서 service메소드를 호출한 후 클리아언트의 GET, POST여부에 따라 doGet() 또는 doPost()를 호출합니다.
4. doGet() or doPost() 메소드는 동적 페이지를 생성한 후 HttpServletResponse객체에 응답을 보냅니다.
5. 응답이 끝나면 HttpServletRequest, HttpServletResponse 두 객체를 소멸시킵니다.

### 생명주기

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## 변수
### 정적변수
### 전역변수

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## 접근제어자
|접근제한|적용대상|접근할 수 없는 클래스|
|-|-|-|
|public|클래스,필드,생성자,메소드|없음|
|protected|필드,생성자,메소드|자식 클래스가 아닌 다른 패키지에 속한 클래스|
|default|클래스,필드,생성자,메소드|다른 패키지에 속한 클래스|
|private|필드,생성자,메소드|모든 외부 클래스|

OOP의 특징중에서 캡슐화라는 개념을 적용하기 위해서 사용한다. 캡슐화를 통하여 결합도를 낮추기 위해서 사용한다.

## 직렬화
객체를 입력 및 출력하기 위해서는 byte 배열로 만드는 과정이 필요한데, 이 과정을 직렬화(Serialize)라고 한다. 반대로 직렬화 되어 있는 byte 코드를 원래의 객체의 형태로 만드는 것을 역직렬화(Deserialize)라고 한다.

### SerialVersionUID
SerialVersionUID를 지정하지 않으면 컴파일러가 임의로 계산한 값을 class에 부여한다. 즉, 컴파일러에 따라 할당되는 값이 다를 수 있고, 이 값은 같은 환경에서도 클래스의 변경이 있으면 달라질 수 있다.문제는 이 값이 다르면 InvalidClassException이 발생하여 역직렬화가 불가능해진다.  그렇기 때문에 이러한 상황을 방지하기 위해서 SerialVersionUID를 지정하는 것이다.


[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## Wrapper Class
primary 타입의 데이터를 reference 형으로 다루기 위해서 사용하는 클래스이다. 그래서 값을 비교하기 위해 == 연산자는 사용할 수 없고 equals()메소드를 사용하여 비교하여야 한다. 다른 특징으로는 Immutable 오브젝트이기 때문에 값을 변경할 경우 새로운 객체가 할당된다.
### String은 래퍼클래스인데 == 비교시 값 같게 나오는 이유
String은 Reference 타입이지만 string pool이라는 영역에 string 객체를 저장해놓기 때문에 리터럴로 사용할 경우에는 intern()메소드를 호출하여 string pool의 내부에서 검색하여 == 으로 같은 값을 찾을 수 있다. 하지만 만약 new 를 사용하여 생성할 경우에는 heap 영역에 저장되어 equals로 비교하여야 한다.

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## 제너릭
클래스의 내부에서 사용할 데이터의 타입을 정의하지 않고 사용할 때 클래스 타입을 받아오도록 하는 것이다. 데이터를 제너릭으로 사용할 때는 항상 레퍼런스 타입으로 가져와야한다.
[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## Final
- final class: 다른 클래스에서 상속하지 못한다.
- final method: 다른 메소드에서 오버라이딩하지 못한다.
- final variable: 변하지 않는 상수가 되어 새로 할당할 수 없는 변수가 된다.

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## 자바 버전
1. JAVA8
- 람다표현식을 사용한다.  
함수형으로 표현할수 있게 해준것이다.
- stream의 추가  
병렬처리가 가능하다.
- 인터페이스 내에 default 메소드 구현 가능
- Optional  
null이 될 수 있는 객체를 감싸는 래퍼 클래스이다.
2. JAVA11
- String, File 클래스 내에 메소드 추가
- 람다에 var 표현 추가
- 자바 표준 HttpClient 추가

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## Static
static은 정적이라는 의미로 메모리 할당을 1회만 수행한다. 해당 데이터를 공유하기 위한 목적으로 많이 사용한다. 메소드에 static이 붙을 시에는 해당 메소드 안에서는 인스턴스 변수 접근이 불가능하며, static 변수만이 static 메소드에 접근할 수 있다.

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## Annotation
일종의 메타데이터로 컴파일 과정과 실행 과정에서 코드를 어떻게 컴파일하고 처리할 것인지 알려주는 정보이다. 어노테이션 그 자체로는 주석에 가까운 표식이지만, 리플렉션을 이용해 어노테이션 적용 여부와 엘리먼트 값을 읽고 처리할 수 있다.

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## 동기화 메소드
동기화 메소드는 한 스레드가 작업 중인 객체에 다른 스레드가 접근할 수 없도록 잠금을 걸어두는 기능(동기화)을 제공하는 메소드이다.

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />
