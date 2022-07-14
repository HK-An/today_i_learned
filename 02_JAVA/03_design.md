# JAVA의 디자인 관련

## 목차
1. [MVC 패턴에서의 `DTO`, `VO`, `Entity`](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/03_design.md#MVC-패턴에서의-DTO-VO-Entity)
    1. [DTO](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/03_design.md#dtodata-transfer-object)
    2. [VO](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/03_design.md#vovalue-object)
    3. [Entity](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/03_design.md#entity)
    4. [Entity와 DTO를 분리하는 이유](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/03_design.md#Entity와-DTO를-분리하는-이유)



## MVC 패턴에서의 `DTO`, `VO`, `Entity`
### DTO(Data Transfer Object)
> 계층간의 데이터 교환만을 위하여 만들어지는 오브젝트

- 계층(Layer)간 데이터 교환이 이루어질 수 있도록 하는 객체이다.
- 여기서 말하는 계층은 Controller, View, 비즈니스 계층, Persistent 계층을 의미하며 JSON Serialization 등에도 사용된다.
- 가변객체이며 데이터 핸들링을 제외한 비즈니스 로직은 포함되어서는 안된다.

### VO(Value Object)
> 단순한 개체를 표현하는 작은 오브젝트의 단위이며 값 자체를 표현

- 단순한 개체를 표현하는 작은 오브젝트의 단위이며, 값 자체를 표현한다.
- setter메서드는 가지지 않지만, getter 메서드와 비즈니스 로직은 포함할 수 있다.
- 내용물이 값 자체를 의미하기 때문에 VO의 값은 변경 불가능하여야한다.
- VO는 객체들의 주소 값이 달라도 데이터 값이 같으면 동일한 것으로 여긴다.
- 필요한 경우 값 비교를 위해 equals()와 hashCode() 메서드를 오버라이딩 해줘야한다.

### Entity
> JPA에서 사용하는 Entity는 DB table과 매핑되는 JAVA의 클래스의 한 종류

- DB 내에 실존하는 table과 매핑되는 개념적으로 존재하는 JAVA 클래스 중의 하나라고 볼 수 있다.
- DB의 Table과 1:1로 매핑되며, table이 가지는 column만을 필드로 가져야한다.
- DB 영속성의 목적으로 사용되는 객체이며, 때문에 요청이나 응답 값을 전달하는 클래스로 사용하는 것은 지양해야한다.
- setter 메서드의 사용을 지양하며, 한번 만들어진 객체는 소멸시까지 불변하다.
- 객체 생성을 위하여 생성자 또는 Builder를 사용한다.
- 다음과 같은 상태를 지닌다.
    - **비영속(New)**: 트랜잭션 구간에 이르기 전까지는, 평범한 Java의 객체이다.
    - **영속(Managed)**: 트랜잭션 구간동안 Entity는 영속 상태가 되며 같은 키를 사용하는 객체들의 동일성을 보장, 지연된 쓰기, 변경사항 자동 업데이트 등의 특징을 지닌다.
    - **준영속(Detached)**: 비영속 상태와 유사하며, Entity 커밋 후 트랜잭션 구간에서 빠져나오는 경우 Entity는 준영속 상태가 된다.
    - **삭제(Removed)**: 관련 method에 의해 삭제될 경우, 매핑된 데이터와 Entity는 삭제 상태가 된다.

### Entity와 DTO를 분리하는 이유
1. DB와 View 사이의 역할 분리를 위해서이다.
2. DTO는 각 계층끼리 주고받는 상자의 개념이며 그 목적은 전달이므로 읽고 쓰는 것이 모두 강하며 일회성으로 사용된다.
3. Entity 객체는 단순히 데이터를 담는 객체가 아니라 DB와도 관련된 중요한 역할을 하며, 일회성이 아니다.
