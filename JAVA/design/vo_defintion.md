# VO (Value Object)
###### 작성일 : 2022년 06월 03일
## 개요
VO는 컴퓨터 과학에서 유일성에 기반하지 않는 단순한 개체를 표현하는 작은 오브젝트의 단위이다. 이 VO 객체는 값 자체를 표현한다. 

## 특징
1. [DTO](https://github.com/HK-An/today_i_learned/blob/main/JAVA/design/dto_defintion.md)처럼 setter메서드는 가지지 않지만, getter 메서드와 비즈니스 로직은 포함할 수 있다.
2. 내용물이 값 자체를 의미하기 때문에 VO의 값은 변경 불가능하여야한다.
3. VO는 객체들의 주소 값이 달라도 데이터 값이 같으면 동일한 것으로 여긴다.
4. 필요한 경우 값 비교를 위해 equals()와 hashCode() 메서드를 오버라이딩 해줘야한다.