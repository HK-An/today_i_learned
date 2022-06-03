# Entity
###### *작성일 : 2022.06.02*      

## 개요
Entity는 [JPA(차후추가예정)](#)에서 사용되는 개념이다. Entity는 DB내에 실존하는 대상이 아니며, DB 내에 실존하는 table과 매핑되는 개념적으로 존재하는 JAVA 클래스 중의 하나라고 볼 수 있다.

## Entity의 상태
1. 비영속(New)
Entity를 생성한 시점부터 트랜잭션 구간에 이르기 전까지는, Entity는 DB와 어떠한 관계도 가지지 않는 평범한 Java의 객체이다.
2. 영속(Managed)
Entity가 트랜잭션 구간에 진입하면, 트랜잭션 구간동안 Entity는 영속 상태가 된다. 이 상태에서 다음과 같은 특징을 지니게 된다.
   - 1차 캐시 사용
   - 같은 키(식별값)를 사용하는 여러 객체의 동일성 보장
   - 지연된 스기와 변경사항 자동 업데이트
3. 준영속(Detached)
비영속 상태와 유사하며, Entity 커밋 후 트랜잭션 구간에서 빠져나오는 경우 Entity는 준영속 상태가 된다.
4. 삭제(Removed)
Entity가 트랜잭션 구간 내에서 관련 method에 의해 삭제될 경우, 매핑된 데이터와 Entity는 삭제 상태가 된다. 객체를 재활용 할 수는 있으나, 권장되지는 않는다.

## Entity Manager
Entity Manager는 Entity를 관리하는 객체이며, 영속성을 가진 Entity의 CRUD를 담당한다. Manager는 Entity관리를 위해 DB 세션과 밀접한 연관성을 가지기 떄문에, 하나의 Manager를 여러 thread에서 사용하는 것은 위험하며, Entity Manager Factory를 공유하여 각 thread에서 Manager를 생성하는 방식이 권장된다.

## 주의할 점
1. DB의 Table과 1:1로 매핑되며, table이 가지는 column만을 필드로 가져야한다.
2. DB [영속성(persistent) (차후추가예정)](#)의 목적으로 사용되는 객체이며, 때문에 요청(Request)이나 응답(Response) 값을 전달하는 클래스로 사용하는 것은 지양해야한다.
4. setter 메서드의 사용을 지양한다.
   - 변경되지 않는 인스턴스에 대해서도 setter로 접근이 가능해지기 때문에 객체의 일관성, 안전성을 보장하기 힘들어지기 때문이다.
   - setter 메소드 대신 생성자 혹은 Builder을 사용한다.
   - 그로 인해 한번 만들어진 객체는 불변하다.
