# Interface

## 개요
인터페이스는 자바에서 클래스들이 구현하여야 하는 메소드를 지정하여 주는 추상 자료형이다. 즉, 동일한 기능을 수행하게끔 하기 위하여 메소드를 추상적으로 미리 정의하여 다형성을 극대화시키는 기능이다.

## 기능
- 상수: 인터페이스에서 값을 미리 정해놓아 참조만 가능하게끔 강제시킨다.
- 추상메소드: 상세적인 기능은 정의하지 않고, 파라미터와 리턴형, 메소드 이름만 정의하여 개발자가 상황에 맞추어 알아서 구현하게끔 한다.
- default 메소드: 인터페이스에서 기본적으로 기능을 구현했지만, 필요시 개발자가 재정의하여 상황에 맞추어 구현하게끔 한다.
- 정적메소드: 인터페이스에서 구현한 기능을 강제적으로 사용하게끔 한다.

## 예시
```java
public interface Bank {
  // 출처: https://limkydev.tistory.com/197
	//상수 (최대 고객에게 인출해 줄 수 있는 금액 명시)
	public int MAX_INTEGER = 10000000;

	//추상메소드(인출하는 메소드)
	void withDraw(int price);

	//추상메소드(입금하는 메소드)
	void deposit(int price);

	//JAVA8에서 가능한 defualt 메소드(고객의 휴면계좌 찾아주는 메소드 : 필수구현은 선택사항)
	default String findDormancyAccount(String custId){
		System.out.println("**금융개정법안 00이후 고객의 휴면계좌 찾아주기 운동**");
		System.out.println("**금융결제원에서 제공하는 로직**");
		return "00은행 000-000-0000-00";
	}

	//JAVA8에서 가능한 정적 메소드(블록체인 인증을 요청하는 메소드)
	static void BCAuth(String bankName){
		System.out.println(bankName+" 에서 블록체인 인증을 요청합니다.");
		System.out.println("전 금융사 공통 블록체인 로직 수행");
	}


}
```

> 참조  
> https://limkydev.tistory.com/197
