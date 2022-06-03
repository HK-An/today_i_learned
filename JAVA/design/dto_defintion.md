# DTO; Data Transfer Object
###### 작성일 : 2022년 06월 03일

## 개요
DTO;Data Tasfer Object는 계층(Layer)간 데이터 교환이 이루어질 수 있도록 하는 객체이다. 여기서 말하는 계층은 Controller, View, 비즈니스 계층, Persistent 계층을 의미하며 JSON Serialization 등에도 사용된다.

## 유래
DTO는 원래 DAO(Data Access Object) 패턴에서 유래된 단어로 DAO에서 DB 처리 로직을 숨기고 DTO라는 결괏값을 내보내는 용도로 활용되었다..

## 특징
1. DTO에 저장된 값을 가져오는 getter 메소드와 DTO에 값을 세팅하는  setter 메서드를 포함하며, 이 외의 비즈니스 로직은 포함하지 않는다.
2. Controller 같은 클라이언트 단과 직접 마주하는 계층에서는 Entity 대신 DTO를 사용해서 데이터를 교환한다.
3. Controller 외에도 여러 레이어 사이에서 DTO를 사용할 수 있지만 주로 View와 Controller 사이에서 데이터를 주고받을 때 활용성이 좋다..
4. 가변 객체로 사용된다.