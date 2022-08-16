# 데이터베이스
## 목차
1. [DBMS](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/03_database.md#dbms)
  1. [DBMS 구조](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/03_database.md#dbms-구조)
  1. [질의처리기 작동 순서](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/03_database.md#질의처리기-작동-순서)
  1. [옵티마이저](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/03_database.md#옵티마이저)
  1. [DB 저장 공간](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/03_database.md#db-저장-공간)
  1. [DBMS Join 원리 종류](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/03_database.md#dbms-join-원리-종류)
  1. [JDBC, ODBC차이](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/03_database.md#jdbc-odbc차이)
  1. [DDL, DML, DCL](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/03_database.md#ddl-dml-dcl)
1. [Key](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/03_database.md#key)
  1. [인덱스](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/03_database.md#인덱스)
    1. [클러스터드, 넌클러스터드 인덱스](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/03_database.md#클러스터드-넌클러스터드-인덱스)
    1. [클러스터](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/03_database.md#클러스터)
    1. [시퀀스](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/03_database.md#시퀀스)
    1. [뷰](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/03_database.md#뷰)
    1. [트리거](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/03_database.md#트리거)
    1. [무결성](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/03_database.md#무결성)
      1. [무결성 보장방법](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/03_database.md#무결성-보장방법)
      1. [정규화](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/03_database.md#정규화)
      1. [정규형 필요 조건](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/03_database.md#정규형-필요-조건)
      1. [함수적 종속성](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/03_database.md#함수적-종속성)
      1. [반정규화](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/03_database.md#반정규화)
    1. [Anomaly](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/03_database.md#anomaly)
    1. [SQL Injection](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/03_database.md#sql-injection)
1. [파티셔닝](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/03_database.md#파티셔닝)
  1. [샤딩](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/03_database.md#샤딩)
  1. [리플리케이션](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/03_database.md#리플리케이션)
  1. [클러스터링](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/03_database.md#클러스터링)
1. [트랜잭션 특징 ACID](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/03_database.md#트랜잭션-특징-acid)
  1. [트랜잭션 상태](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/03_database.md#트랜잭션-상태)
  1. [트랜잭션 격리 종류](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/03_database.md#트랜잭션-격리-종류)
  1. [낮은 격리단계 선택시 발생 문제](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/03_database.md#낮은-격리단계-선택시-발생-문제)
1. [Persistence Layer](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/03_database.md#persistence-layer)
1. [UML](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/03_database.md#uml)
1. [MySQL 특징](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/03_database.md#mysql-특징)
1. [PostgreSQL 특징](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/03_database.md#postgresql-특징)
1. [SQL vs NOSQL](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/03_database.md#sql-vs-nosql)
  1. [CAP 이론](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/03_database.md#cap-이론)
  1. [NoSQL 종류](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/03_database.md#nosql-종류)
  1. [Redis](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/03_database.md#redis)
  1. [카산드라 특징 ](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/03_database.md#카산드라-특징)

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
### DDL, DML, DCL

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## Key
### 인덱스
#### 클러스터드, 넌클러스터드 인덱스
#### 클러스터
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

## 파티셔닝
테이블을 단위로 나누어 관리하는 기법 흔히 그냥 파티셔닝이라고 한다면 컬럼별로 나누는 Vertical Partitioning을 의미한다.

> 파티셔닝은 테이블을 컬럼 단위로 나누는 기법인데요. 장점은 update나 insert 같은 작업이 분산되어서 성능이 향상되구요. 단점은 테이블간 join 비용이 증가하게 되고, index를 별도로 파티셔닝할 수 없다는 단점을 가지고 있습니다.

### 샤딩
테이블을 로우 단위로 나누는 것 (Horizontal Partitioning)

- Hash Sharding
간단하고 빠르지만 확장이 힘들다.

- Dynamic Sharding
특정 범위에 따라 샤딩을 한다.

> 샤딩은 테이블을 row단위로 분산해서 저장하는 방법입니다. Horizontal Partitioning이라고도 하는데요 샤드 key를 정하는 방법에 따라서 샤드 종류가 결정되는데 크게 Hash Sharding과 Dynamic Sharding이 있습니다.

### 리플리케이션
### 클러스터링



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

## Persistence Layer

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## UML

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## MySQL 특징

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## PostgreSQL 특징
1. 관계형 모델  
기존의 RDBMS가 가지고 있는 거의 모든 기능을 가지고 있다.
2. 고수준 확장성  
사용자 정의 오퍼레이터와 타입, 함수, 엑세스 메소드를 지원한다. 또한 파이썬 등을 절차적 언어로 사용할 수 있다.
3. 객체지향  
상속, 객체 등이 구현되어있다.
7. 국제화, 텍스트 검색

> PostgreSQL은 대용량의 복잡한 트랜잭션 처리를 위한 RDBMS입니다. PostgreSql의 대표적인 특징으로는 관계형모델, 고수준 확장성, 객체지향 등의 특징을 지니고 있습니다.

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

> NOSQL은 Not Only SQL의 약자로 SQL을 보완한다는 의미를 가지고 있습니다.
NOSQL은 스키마가 없어서 데이터를 조회하고 삽입하는 속도가 빠릅니다.
또한 대량의 분산 데이터를 저장하는데 특화되어있습니다.

### CAP 이론
### NoSQL 종류
### NoSQL 사용경험
### Redis
### 카산드라 특징 

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />
