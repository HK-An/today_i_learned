# 영속성 (Persistence)
###### 작성일 : 2022년 06월 11일

## 개요
- 데이터를 생성한 어플리케이션이 종료되어도 사라지지 않는 데이터의 특성을 말한다.
- 영속성을 갖지 않는 데이터는 메모리에서만 존재하기 때문에 어플리케이션을 종료 시, 해당 데이터는 휘발된다. (작성하던 문서를 저장하지 않고 종료하는 것과 같음)

## Object Persistence (영구 객체)
메모리 상의 데이터를 파일 시스템, RDB 혹은 객체 데이터베이스 등을 통하여 영구적으로 기억장치에 저장해 영속성을 부여한다.

## Persistence Layer
- 어플리케이션 구조에서 현재 메모리에 존재하는 데이터들을 저장하여 영속성을 부여해주는 계층을 의미한다.
- JDBC 등을 이용하여 직접 구현할 수도 있지만 편의성 등을 이유로 Framework를 이용하여 개발을 하는 경우가 많다.

## Persistence Framework
- 번거로운 설정 등을 거치지 않고 간단한 환경설정 작업만으로 DB와 연동되는 시스템을 개발할 수 있다.
- Persistence Framework는 크게 SQL Query를 직접 매핑해주는 SQL Mapper와 [ORM](https://github.com/HK-An/today_i_learned/blob/main/CONCEPT/orm/definition.md)으로 나눌 수 있다.
