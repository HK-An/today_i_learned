# Entity
###### *작성일 : 2022.06.02*      

## 개요
Entity는 [JPA(차후추가예정)](#)에서 사용되는 개념이다. Entity는 DB내에 실존하는 대상이 아니며, DB 내에 실존하는 table과 매핑되는 개념적으로 존재하는 JAVA 클래스 중의 하나라고 볼 수 있다.

## 특징
1. DB의 Table과 1:1로 매핑되며, table이 가지는 column만을 필드로 가져야한다.
2. DB [영속성(persistent) (차후추가예정)](#)의 목적으로 사용되는 객체이며, 때문에 요청(Request)이나 응답(Response) 값을 전달하는 클래스로 사용하는 것은 지양해야한다.
4. setter 메서드의 사용을 지양한다.
   - 변경되지 않는 인스턴스에 대해서도 setter로 접근이 가능해지기 때문에 객체의 일관성, 안전성을 보장하기 힘들어지기 때문이다.
   - setter 메소드 대신 생성자 혹은 Builder을 사용한다.
   - 그로 인해 한번 만들어진 객체는 불변하다.