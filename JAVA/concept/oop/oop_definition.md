# 객체지향 (OOP; Object-Oriented Programming)

##  개요
객체지향이란 프로그램 설계방법의 일종으로, 작성한 코드가 순서대로만 실행될 것을 기대하는 절차지향 프로그램과는 다르게, 프로그램을 여러 객체(object)로 나누어 각 객체들이 상호작용 하는 방식의 프로그램 구현 방식이다.

## 주요 요소
### 1. 캡슐화 (Encapsulation)
변수와 함수를 하나로 묶는 것을 의미한다. 이를 통하여 캡슐화 된 객체 외부에서는 내부의 데이터에 대하여 접근을 막을 수 있는데, 이를 정보 은닉(Information hiding)이라고 한다. 이러한 캡슐화를 통하여 각 객체간의 결합도를 떨어트려 유지보수의 용이성을 올릴 수 있다.
```java
class Person {
	private String name;
    private int age;
    
    public void setName(String name) {
    	this.name = name;
    }
    
    public void setAge(int age) {
    	this.age = age;
    } 
    
    public String getName() {
    	return name;
    }
    
    public int getAge() {
    	return age;
    }
}

public class Application() {
	public static void main(String[] args) {
    	Person person = new Person();
        person.age = 20; // age 변수의 private 접근자로 인하여 접근 불가능
        person.setAge(20); // Member class 내부의 setAge()함수가 age 변수에 접근하여 값 변경
    }
}
```

### 2. 상속 (Inheritance)
상속은 자식 클래스가 부모 클래스의 특성과 기능을 그대로 물려받는 것을 의미한다. 상속 받은 기능 중 필요에 의해 일정 부분을 재정의할 경우, 이를 오버라이딩(Overriding)이라고 한다. 상속은 캡슐화를 유지하면서 클래스의 재사용이 용이하게 해준다.

```java
.....................
Person class 코드 생략
.....................

Korean extends Person {
    public Korean(String name, int age) {
        setAge(age);
        setName(name);
    }

    public void hello() {
        System.out.println("안녕하세요 저는 " + getName() + "이고, 나이는 " + getAge() + "입니다.");
    }
}
```
### 3. 다형성 (Polymorphism)

하나의 변수나 함수가 상황에 따라 다르게 사용되는 것을 의미하며, 이에 대한 예로 오버로딩(Overloading)과 오버라이딩(Overriding)을 들 수 있다.

```java
public void hello() {
	System.out.println("안녕!");
}

public void hello(String name) {
	System.out.println("안녕! 나는 " + name + "(이)야!");
}

public void hello(String name, int age) {
	System.out.println(안녕! 나는 " + name + "(이)고 " + age + "살이야!");
}

```

### 4. 직렬화/역직렬화 (Serialization/Deserialization)

직렬화란 서버나 다른 프로그램에 전송하기 위해 객체를 바이트 코드로 변환하는 것을 의미하고 역직렬화는 그와 반대로 바이트 코드를 객체로 변환하는 것을 의미한다.  
(직렬화에 대해서는 나중에 별도로 다룰 예정임)

## 주요 원칙

객체지향에는 반드시 지켜야 할 5개의 원칙이 있으며 원칙 각각의 앞글자를 따서 이를 SOLID 원칙이라고 부른다.

### 1. 단일 책임 원칙 (SRP; Single Resposibility Principle)

객체는 각각 하나만의 책임(기능)만을 지녀야 한다.

```java
public void getNameAndSaveUser() {
	... // SRP 위배
}

...................................

// 하나의 메소드는 하나의 역할만 수행하여야 한다.
public void process() {
	String name = getName();
    saveUser(name);
}
```

### 2. 개방-폐쇄 원칙 (OCP; Open-Closed Principle)

객체는 확장에 대해서는 개방적이고 수정에 대해서는 폐쇄적이야한다. 즉, 기능의 확장은 지향해야하지만, 본연의 의미에 대한 변경은 폐쇄적으로 접근해야 한다.

```java
class Person {
	public void hello() {
    	System.out.println("Waving hand"); // 손을 흔들며 인사함
    }
}

class Korean extends Person {

	// 오버라이딩을 통한 기능의 확장
	@Override
    public void hello() {
    	bow(); // 허리를 숙이며 인사
    	System.out.println("안녕하세요");
    }
    
    private void vow() {
    	...
    }
}
```

### 3. 리스코프 치환 원칙 (LSP; Liskov Substitution Principle)

자식 클래스는 언제나 부모 클래스를 대신할 수 있어야 한다는 원칙이다. 특히, 상속과 관련된 중요 원칙인데 상속은  `상위계층`->`하위계층`으로 가는 것이 아닌,  `상위분류`->`하위분류`의 형태로 이루어져야 한다.

> Daddy james = new Son(); // LSP 미충족  
> Person korean = new Korean(); // LSP 충족

### 4. 인터페이스 분리 원칙 (ISP; Interface Segregation Principle)

구현된 클래스에서 사용하지 않는 메서드는 존재하면 안된다는 원칙.

```java
interface Animal {
	public void eat();
    public void fly();
    public void sleep();
}

class Human implements Animal{
	public void move() {
    	walk(); // 사람은 날 수 없으므로 fly() 메소드는 사용되지 않음. ISP 위배
    }
}
```

### 5. 의존성 역전 원칙 (DIP; Dependency Inversion Principle)

추상성이 높고 안정적인 고수준의 클래스는 구체적이고 불안정한 저수준의 클래스를 참조해서는 안된다는 원칙으로, 일반적으로 OOP에서 사용하는 인터페이스의 기능으로 이를 해결이 가능하다.

> Animal <- Human ( o )  
> Animal -> Human ( x )