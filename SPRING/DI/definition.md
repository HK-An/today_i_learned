# DI;Dependency Injection (의존성 주입)

###### 작성일: 2022년 6월 17일

## 개요
의존성 주입은 객체가 외부 요소에 의하여 의존성이 주입되는 패턴을 말한다.   
객체 내부에서 다른 객체를 생성하지 않고, 외부에서 생성된 객체를 넘겨받는 것은 결합도를 낮출 수 있고, 유연한 관계를 기대할 수 있게 된다.

## 예제코드
### 1. 의존성 주입을 하지 않은 코드
```java
public class Burger {...}

public class Restaurant {
  private Burger burger = new Burger();

  public void newBurgerOrder() {
    this.burger.make();
  }
}
```
위의 코드는 햄버거를 만들어서 판매하는 레스토랑을 구현한 코드이다. 이 레스토랑은 기본적인 햄버거 레시피를 가지고 있다.  
 위 코드에서 Restaurant 객체는 Burger 객체를 생성하며, `Restaurant 객체는 Burger 객체에 의존`하게 된다.  
만약, 이 레스토랑이 기본적인 햄버거 레시피에 재료를 추가하여 치즈버거나 기타 다른 햄버거 레시피를 개발하여 판매하고자 하면 위 코드는 수정되어야 할 것이고, 이는 결국 코드 전체의 유지보수 비용 증가로 이어지게 된다.

### 2. 일반적인 의존성 주입을 한 코드
```java
public class Burger {...}
public class CheezeBurger extends Burger {...}
public class BeefBurger extends Burger {...}

public class Restaurant {
  private Burger burger;

  public Restaurant(Burger burger) {
    this.burger = burger;
  }
  public void newBurgerOrder() {
    this.burger.make();
  }
}
```
1번 코드에서 발견한 문제점을 해결하기 위하여 Restaurant 객체에 Burger 객체를 `주입`해주었다.  
객체를 내부에서 생성해주지 않고, 주입해준 덕분에 이 레스토랑은 Burger 객체를 상속할 수 있는 레시피라면, Restaurant 객체를 수정하지 않고 코드를 지속적으로 재사용할 수 있을 것이다.

### 3. Spring 환경에서 사용하는 의존성 주입
스프링 환경에서 사용할 수 있는 의존성 주입 방법으로는 생성자 주입, 수정자 주입, 필드 주입의 3가지 방법이 있으며 그 중 `생성자주입`을 가장 추천한다.

#### 3.1. 생성자 주입(Constructor Injection)
```java
@Service
public class RestaurantServiceImpl implements RestaurantService {
  private RecipeRepository recipeRepository;

  @Autowired
  public RestaurantServiceImpl(RecipeRepository recipeRepository) {
    this.recipeRepository = recipeRepository;
  }
  ...
}
```
생성자 주입은 생성자의 특성으로 인하여 객체 호출 시점에 1회만 호출되는 것이 보장되며, 생성자가 1개일 경우 `@Autowired`는 생략이 가능하다.  
주입받는 객체가 변하지 않거나, 반드시 객체의 주입이 필요한 경우에 강제하기 위하여 사용한다.  
의존성 주입 방법 중 생성자 주입을 추천하는 이유를 간단하게 설명하면 다음과 같다.
- NullPointerException을 방지할 수 있다.
- 주입받을 필드를 final로 선언 가능하다.
- 순환참조를 방지할 수 있다.
- 테스트 코드 작성에 유리하다.
- 객체의 불변성을 확보할 수 있다.

#### 3.2. 수정자 주입(Setter Injection)
```java
@Service
public class RestaurantServiceImpl implements RestaurantService {
  private RecipeRepository recipeRepository;

  @Autowired
  public void setRecipeRepository(RecipeRepository recipeRepository) {
    this.recipeRepository = recipeRepository;
  }
  ...
}
```
수정자 주입은 Setter를 이용하여 의존관계를 주입하는 방법으로 주입하는 객체가 변할 수 있는 경우에 사용한다. 만약 `@Autowired`로 주입할 대상이 없는 경우에는 오류가 발생한다.

#### 3.3. 필드 주입(Field Injection)
```java
@Service
public class RestaurantServiceImpl implements RestaurantService {
  @Autowired
  private RecipeRepository recipeRepository;
  ...
}
```
필드 주입은 필드에 바로 의존 관계를 주입하는 방법이다. 가장 간단하며 코드가 간결해져 많이 사용하였으나, 외부에서 의존성 주입을 통제할 수 없어 지양하는 추세이다.


> 참조
> https://ko.wikipedia.org/wiki/%EC%9D%98%EC%A1%B4%EC%84%B1_%EC%A3%BC%EC%9E%85
> https://tecoble.techcourse.co.kr/post/2021-04-27-dependency-injection/
> https://velog.io/@jeong-god/DI%EB%9E%80-%EB%AC%B4%EC%97%87%EC%9D%B8%EA%B0%80
> https://yaboong.github.io/spring/2019/08/29/why-field-injection-is-bad/
