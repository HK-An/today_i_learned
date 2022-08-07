# 데이터베이스
## 목차
1. [DBMS란?]()
  1. [DBMS 구조]()
  1. [질의처리기 작동 순서]()
  1. [옵티마이저]()
  1. [DB 저장 공간]()
  1. [DBMS Join 원리 종류]()
  1. [JDBC, ODBC차이]()
  1. [DDL, DML, DCL?]()
1. [Key]()
  1. [인덱스]()
    1. [클러스터드, 넌클러스터드 인덱스란?]()
    1. [클러스터란?]()
    1. [시퀀스]()
    1. [뷰]()
    1. [트리거]()
    1. [무결성]()
      1. [무결성 보장방법]()
      1. [정규화]()
      1. [정규형 필요 조건]()
      1. [함수적 종속성]()
      1. [반정규화]()
    1. [Anomaly]()
    1. [SQL Injection]()
1. [파티셔닝이란?]()
  1. [샤딩이란]()
  1. [리플리케이션이란?]()
  1. [클러스터링이란?]()
1. [트랜잭션 특징 ACID]()
  1. [트랜잭션 상태]()
  1. [트랜잭션 격리 종류]()
  1. [낮은 격리단계 선택시 발생 문제]()
1. [Persistence Layer란?]()
1. [UML]()
1. [MySQL 특징]()
1. [PostgreSQL 특징]()
1. [SQL vs NOSQL]()
  1. [CAP 이론]()
  1. [NoSQL 종류]()
  1. [NoSQL 사용경험]()
  1. [Redis란?]()
  1. [카산드라 특징 ]()

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## DBMS
데이터베이스 내 데이터에 접근하도록 도와주는 시스템

> DBMS는 데이터베이스 내 데이터에 접근하도록 도와주는 시스템입니다. DBMS는 크게 질의처리기와 저장시스템으로 이루어져 있습니다.

### DBMS 구조
### 질의처리기 작동 순서
### 옵티마이저
### DB 저장 공간
### DBMS Join 원리 종류
### JDBC, ODBC차이
### DDL, DML, DCL?

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## Key
### 인덱스
#### 클러스터드, 넌클러스터드 인덱스란?
#### 클러스터란?
### 시퀀스
### 뷰
### 트리거
### 무결성
#### 무결성 보장방법
### 정규화
#### 정규형 필요 조건
#### 함수적 종속성
#### 반정규화
### Anomaly
### SQL Injection

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## 파티셔닝이란?
테이블을 단위로 나누어 관리하는 기법 흔히 그냥 파티셔닝이라고 한다면 컬럼별로 나누는 Vertical Partitioning을 의미한다.

> 파티셔닝은 테이블을 컬럼 단위로 나누는 기법인데요. 장점은 update나 insert 같은 작업이 분산되어서 성능이 향상되구요. 단점은 테이블간 join 비용이 증가하게 되고, index를 별도로 파티셔닝할 수 없다는 단점을 가지고 있습니다.

### 샤딩이란
테이블을 로우 단위로 나누는 것 (Horizontal Partitioning)

- Hash Sharding
간단하고 빠르지만 확장이 힘들다.

- Dynamic Sharding
특정 범위에 따라 샤딩을 한다.

> 샤딩은 테이블을 row단위로 분산해서 저장하는 방법입니다. Horizontal Partitioning이라고도 하는데요 샤드 key를 정하는 방법에 따라서 샤드 종류가 결정되는데 크게 Hash Sharding과 Dynamic Sharding이 있습니다.

### 리플리케이션이란?
### 클러스터링이란?



[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## 트랜잭션 특징 ACID
A: 원자성 C: 일관성 I: 격리성 D: 지속성

> 데이터베이스의 무결성과 일관성을 위해서 트랜잭션은 4가지 특징을 만족해야되는데요. 원자성은 한 트랜잭션내 실행한 작업은 모두 성공하거나 실패해야하는 것이고, 일관성은 일관성있는 데이터베이스의 상태를 유지시키는 것입니다. 그리고 격리성은 동시에 실행되는 트랜잭션은 서로에게 영향을 미치지 않아야 되고, 지속성은 트랜잭션 완료시 결과가 영구적으로 반영되어야 합니다.

### 트랜잭션 상태
### 트랜잭션 격리 종류
### 낮은 격리단계 선택시 발생 문제

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## Persistence Layer란?

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## UML

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## MySQL 특징

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## PostgreSQL 특징

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## SQL vs NOSQL
- SQL
=RDBMS

- NOSQL
Not Only SQL의 약자로 SQL을 보완한다는 의미

- SQL vs NOSQL
가장 큰 차이는 스키마(테이블 데이터를 저장하는 규칙)가 있냐 없냐
SQL은 기존에 저장한거 참조해서 관계를 지정하지만 NOSQL은 그냥 필요한거 그대로 저장해버림 관계

> NOSQL은 Not Only SQL의 약자로 SQL을 보완한다는 의미를 가지고 있습니다. NOSQL은 스키마가 없어서 데이터를 조회하고 삽입하는 속도가 빠릅니다. 또한 대량으 ㅣ분산 데이터를 저장하는데 특화되어있습니다.

### CAP 이론
### NoSQL 종류
### NoSQL 사용경험
### Redis란?
### 카산드라 특징 

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />
