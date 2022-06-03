# 정리
1. [VO](https://github.com/HK-An/today_i_learned/blob/main/JAVA/design/vo_defintion.md): 단순한 개체를 표현하는 작은 오브젝트의 단위이며 값 자체를 표현함. 약간의 비즈니스 로직은 구현가능하지만 수정불가.
2. [DTO](https://github.com/HK-An/today_i_learned/blob/main/JAVA/design/dto_defintion.md): 계층간의 데이터 교환을 위하여 만들어지는 오브젝트이며 가변적이지만 데이터 핸들링을 제외한 비즈니스 로직은 포함되어서는 안됨.
3. [Entity](https://github.com/HK-An/today_i_learned/blob/main/JAVA/design/entity_definition.md): JPA에서 사용하는 Entity는 DB table과 매핑되는 JAVA의 클래스의 한 종류임.

# Entity와 DTO를 분리하는 이유
1. DB와 View 사이의 역할 분리를 위해서이다.
2. DTO는 각 계층끼리 주고받는 상자의 개념이며 그 목적은 전달이므로 읽고 쓰는 것이 모두 강하며 일회성으로 사용된다.
3. Entity 객체는 단순히 데이터를 담는 객체가 아니라 DB와도 관련된 중요한 역할을 하며, 일회성이 아니다.
4. 실사용시 실제 View에서 요청되는 정보와 테이블에 매핑되는 정보가 달라 데이터를 변환하는 로직이 필요할 수 있는데, 이렇게 될 경우 Entity에 해당 로직이 들어가는 것은 깔끔하지 못함.
5. 전체 작업 규칙에 맞춰서 개발하는 것이 가장 유동적인 방법임.