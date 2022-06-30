# IOC;Inversion of Control
###### 작성일: 2022년 06월 30일
## 개요
IOC는 말 그대로 "제어의 역전"이라는 뜻으로 메소드나 객체의 호출작업을 개발자가 결정하는 것이 아니라, 외부에서 결정되는 디자인 패턴을 의미한다.

## 예제코드

```java
public class Car {
  private Gear gear;
  private Tire tire;

  public Car() {
    gear = new Gear();
    tire = new Tire();
  }

  public void move(){
    gear.setGear(1);
    tire.rotate();
  }
  // ...
}
```
IOC가 이루어지지 않은 코드는 위와 같이 이루어진다.

하지만 스프링에서 제공하는 @Autowired 어노테이션을 활용하면 개발자가 직접 의존관계를 설정해주지 않고 프레임워크의 의존관계의 제어를 맡길 수 있다.
```java
public class Car {
  private Gear gear;
  private Tire tire;

  @Autowired
  public Car(Gear gear, Tire tire) {
    this.gear = gear;
    this.tire = tire
  }

  public void move(){
    gear.setGear(1);
    tire.rotate();
  }
  // ...
}
```

##### 참고
>https://ko.wikipedia.org/wiki/%EC%A0%9C%EC%96%B4_%EB%B0%98%EC%A0%84  
>https://beststar-1.tistory.com/33
