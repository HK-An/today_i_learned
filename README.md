# :green_book: Today_What_I_Learned
공부한 내용을 정리해놓은 것들.

## Git Commit 메세지용 Emoji
|icon|cmd|설명|
|-|-|-|
|:pick:|:pick|신규 내용 추가|
|:hammer_and_wrench:|:hammer_and_wrench|기존 내용 수정|
|:x:|:x|삭제|

## :link: 바로가기
- [개념정리](https://github.com/HK-An/today_i_learned#school-computer_science)
- [Java관련](https://github.com/HK-An/today_i_learned#space_invader-java)
- [Spring관련](https://github.com/HK-An/today_i_learned#leaves-spring)
- [RDB관련](https://github.com/HK-An/today_i_learned#floppy_disk-rdb)
- [알고리즘관련](https://github.com/HK-An/today_i_learned#1-algorithm)
- [코딩문제풀이](https://github.com/HK-An/today_i_learned#bangbang-코딩문제풀이)
***
# :school: COMPUTER_SCIENCE
### OS [(보러가기)](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/01_OS.md)
<details>
  <summary>접어두기</summary>

- 운영체제란
  - 실행파일 실행 과정
  - 프로그램 실행 과정
- 캐시
- 캐시라인
- 메모리 구조
  - 전역변수와 정적변수의 차이
  - Heap과 Stack의 비교
  - 가시성과 원자성
  - 유효주소, 주소지정방식
  - 메모리할당, 알고리즘
- 프로세스와 스레드
  - 멀티프로세스와 멀티스레드
  - 스레드와 프로세스 콘텍스트 스위치 차이 이유
  - 프로세스 스케줄러에 대해
  - CPU 스케줄러
  - 스레싱
  - IPC
  - Race Condition
- 가상 메모리
  - 메모리 단편화
  - 페이징기법
  - 세그먼테이션 기법
  - 메모리풀
  - 페이지 교체 알고리즘
  - MMU란
  - TLB란
- 인터럽트란
  - System Call
  - 프로세스 제어 명령
  - fork(), vfork() 차이
  - 시스템콜과 서브루틴 차이
- 블록킹, 논블록킹
- 동기, 비동기
- 동기 IO 처리과정 : 프로세스 A가 디스크에서 어떤 데이터 읽어올때 상황
- 입출력 처리방식
  - DMA
  - Cycle Stealing
- 데드락
  - 발생조건
  - 회피기법
- PCB(Process Control Block) 이란
- Spin Lock 이란

</details>

### 자료구조 [(보러가기)](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/02_data_structure.md)
- stack
- queue
- heap (priority queue)
### WEB [(보러가기)](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/03_web.md.md)
- 브라우저에 url을 치면 일어나는 일
- 쿠키와 세션
  - 쿠키
  - 세션
- REST API, RESTful이란
- HTTP 응답코드
- HTTPS
### 그외
- [리팩토링](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/refactoring/refactoring_definition.md)
- [OOP](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/oop/oop_definition.md)
- [TDD](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/tdd/tdd_definition.md)
- [MVC2](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/mvc/definition.md)
- [오버로딩 vs 오버라이딩](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/overrloading_vs_overriding.md)
- [메모리의구조(코드, 데이터, 힙, 스택 영역)](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/memory/structure.md)
- [해시(자료구조)](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/hash/definition.md)
- [IOC vs DI](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/DI_vs_IOC.md)
***
# :space_invader: JAVA
### 개념 [(보러가기)](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/01_concept.md)
- 자바의 특징
- 자바의 컴파일 과정
- JVM의 구조
- 가비지 컬렉션의 동작흐름
- 클래스
- 객체
- 캡슐화
- 상속
- 다형성
- Static
- Final
- 접근제어자
- 인터페이스 vs 추상클래스
- 어노테이션
- Overloding vs overrloading
- Thread
- 동기화 메소드
- 직렬화와 SerialVersionUID

### 자바의 데이터 타입 및 기타 타입들 [(보러가기)](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/02_type.md)
- 기본 데이터 타입
- 제너릭 타입
- String, StringBuffer, StringBuilder의 차이
- List
- Set
- Map

### 디자인 [(보러가기)](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/03_design.md)
- MVC 패턴에서의 DTO, VO, Entity
    - DTO
    - VO
    - Entity
    - Entity와 DTO를 분리하는 이유

### 기본API
- [java.util.*](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/api/java.util.all.md)
### 기타
- [Stream](https://github.com/HK-An/today_i_learned/blob/main/02_JAVA/streams_definition_and_usage.md)

***
# :leaves: SPRING
- [Spring Secuirty](https://github.com/HK-An/today_i_learned/blob/main/03_SPRING/security/definition.md)
***
# :floppy_disk: RDB
***
# :+1: ALGORITHM [(보러가기)](https://github.com/HK-An/today_i_learned/blob/main/04_ALGORITHM)
- BFS(너비우선탐색)
- DFS(깊이우선탐색)
- 백트래킹
- 시뮬레이션
- 투포인터
- 이진탐색
- MST
- 다익스트라
- [탐욕알고리즘](https://github.com/HK-An/today_i_learned/blob/main/04_ALGORITHM/greedy/definition.md)
- 수학관련
    - [유클리드 호제법을 통한 최대공약수, 최소공배수 구하기](https://github.com/HK-An/today_i_learned/blob/main/04_ALGORITHM/math/euclidean_algorithm.md)

# :bangbang: 코딩문제풀이
### 문제풀이
#### 프로그래머스
<details>
  <summary>Lv1 (Clear!)</summary>

  **LV1 진행률: 100.00%(55/55)**
<img src="https://github.com/HK-An/today_i_learned/blob/main/00_IMGS/05_CODING/programmers/complete-lv1.png">
- [신고결과받기](https://github.com/HK-An/today_i_learned/blob/main/05_CODING/programmers/lv1/report_result.md)    
- [로또의 최고 순위와 최저 순위](https://github.com/HK-An/today_i_learned/blob/main/05_CODING/programmers/lv1/lotto.md)
- [가운데 글자 가져오기](https://github.com/HK-An/today_i_learned/blob/main/05_CODING/programmers/lv1/get_center_character.md)
- [신규 아이디 추천](https://github.com/HK-An/today_i_learned/blob/main/05_CODING/programmers/lv1/id_recommendation.md)
- [2016년](https://github.com/HK-An/today_i_learned/blob/main/05_CODING/programmers/lv1/yerar2016.md)
- [숫자 문자열과 영단어](https://github.com/HK-An/today_i_learned/blob/main/05_CODING/programmers/lv1/converting_game.md)
- [내적](https://github.com/HK-An/today_i_learned/blob/main/05_CODING/programmers/lv1/dot_product.md)
- [키패드 누르기](https://github.com/HK-An/today_i_learned/blob/main/05_CODING/programmers/lv1/pressing_keypad.md)
- [K번째 수](https://github.com/HK-An/today_i_learned/blob/main/05_CODING/programmers/lv1/kth_number.md)
- [크레인 인형뽑기 게임](https://github.com/HK-An/today_i_learned/blob/main/05_CODING/programmers/lv1/claw_crane_game.md)
- [없는 숫자 더하기](https://github.com/HK-An/today_i_learned/blob/main/05_CODING/programmers/lv1/sum_of_absence_number.md)
- [음양 더하기](https://github.com/HK-An/today_i_learned/blob/main/05_CODING/programmers/lv1/positive_and_negative.md)
- [소수 만들기](https://github.com/HK-An/today_i_learned/blob/main/05_CODING/programmers/lv1/making_prime_number.md)
- [체육복](https://github.com/HK-An/today_i_learned/blob/main/05_CODING/programmers/lv1/pe_clothes.md)
- [폰켓몬](https://github.com/HK-An/today_i_learned/blob/main/05_CODING/programmers/lv1/pocketmon.md)
- [모의고사](https://github.com/HK-An/today_i_learned/blob/main/05_CODING/programmers/lv1/trial_exam.md)
- [실패율](https://github.com/HK-An/today_i_learned/blob/main/05_CODING/programmers/lv1/failure_rate.md)
- [약수의 개수와 덧셈](https://github.com/HK-An/today_i_learned/blob/main/05_CODING/programmers/lv1/divisor.md)
- [3진법 뒤집기](https://github.com/HK-An/today_i_learned/blob/main/05_CODING/programmers/lv1/reverse_ternary.md)
- [예산](https://github.com/HK-An/today_i_learned/blob/main/05_CODING/programmers/lv1/budget.md)
- [두 개 뽑아서 더하기](https://github.com/HK-An/today_i_learned/blob/main/05_CODING/programmers/lv1/pick_and_sum.md)
- [최소직사각형](https://github.com/HK-An/today_i_learned/blob/main/05_CODING/programmers/lv1/namecard.md)
- [나머지가 1이 되는 수 찾기](https://github.com/HK-An/today_i_learned/blob/main/05_CODING/programmers/lv1/remain.md)
- [부족한 금액 계산하기](https://github.com/HK-An/today_i_learned/blob/main/05_CODING/programmers/lv1/price_of_rides.md)
- [비밀지도](https://github.com/HK-An/today_i_learned/blob/main/05_CODING/programmers/lv1/secret_map.md)
- [같은 숫자는 싫어](https://github.com/HK-An/today_i_learned/blob/main/05_CODING/programmers/lv1/remove_duplicated.md)
- [다트 게임](https://github.com/HK-An/today_i_learned/blob/main/05_CODING/programmers/lv1/dart_game.md)
- [나누어 떨어지는 숫자 배열](https://github.com/HK-An/today_i_learned/blob/main/05_CODING/programmers/lv1/no_remains.md)
- [두 정수 사이의 합](https://github.com/HK-An/today_i_learned/blob/main/05_CODING/programmers/lv1/sum_of_two_numbers.md)
- [문자열 내 마음대로 정렬하기](https://github.com/HK-An/today_i_learned/blob/main/05_CODING/programmers/lv1/arranging_string.md)
- [문자열 내 p와 y의 개수](https://github.com/HK-An/today_i_learned/blob/main/05_CODING/programmers/lv1/num_of_p_and_y.md)
- [문자열 내림차순으로 배치하기](https://github.com/HK-An/today_i_learned/blob/main/05_CODING/programmers/lv1/arrange_string_desc.md)
- [문자열 다루기 기본](https://github.com/HK-An/today_i_learned/blob/main/05_CODING/programmers/lv1/string_for_biginner.md)
- [소수 찾기](https://github.com/HK-An/today_i_learned/blob/main/05_CODING/programmers/lv1/find_prime_number.md)
- [서울에서 김서방 찾기](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/programmers/src/main/java/kr/hk/lv1/FindingKim.java)
- [수박수박수박수박수박수?](https://github.com/HK-An/today_i_learned/blob/main/05_CODING/programmers/lv1/reiterate.md)
- [문자열을 정수로 바꾸기](https://github.com/HK-An/today_i_learned/blob/main/05_CODING/programmers/lv1/parseInt.md)
- [시저 암호](https://github.com/HK-An/today_i_learned/blob/main/05_CODING/programmers/lv1/ceasar_cipher.md)
- [약수의 합](https://github.com/HK-An/today_i_learned/blob/main/05_CODING/programmers/lv1/sum_of_divisor.md)
- [이상한 문자 만들기](https://github.com/HK-An/today_i_learned/blob/main/05_CODING/programmers/lv1/weird_string.md)
- [자릿수 더하기](https://github.com/HK-An/today_i_learned/blob/main/05_CODING/programmers/lv1/sum_of_digits.md)
- [자연수 뒤집어 배열로 만들기](https://github.com/HK-An/today_i_learned/blob/main/05_CODING/programmers/lv1/reversing_number.md)
- [정수 내림차순으로 배치하기](https://github.com/HK-An/today_i_learned/blob/main/05_CODING/programmers/lv1/int_order_by_desc.md)
- [정수 제곱근 판별](https://github.com/HK-An/today_i_learned/blob/main/05_CODING/programmers/lv1/judge_squart.md)
- [제일 작은 수 제거하기](https://github.com/HK-An/today_i_learned/blob/main/05_CODING/programmers/lv1/removing_smallest.md)
- [짝수와 홀수](https://github.com/HK-An/today_i_learned/blob/main/05_CODING/programmers/lv1/even_and_odd.md)
- [최대공약수와 최소공배수](https://github.com/HK-An/today_i_learned/blob/main/05_CODING/programmers/lv1/gcd_and_lcm.md)
- [콜라츠 추측](https://github.com/HK-An/today_i_learned/blob/main/05_CODING/programmers/lv1/collatz_conjecture.md)
- [평균 구하기](https://github.com/HK-An/today_i_learned/blob/main/05_CODING/programmers/lv1/get_average.md)
- [햐샤드 수](https://github.com/HK-An/today_i_learned/blob/main/05_CODING/programmers/lv1/harshad_number.md)
- [핸드폰 번호 가리기](https://github.com/HK-An/today_i_learned/blob/main/05_CODING/programmers/lv1/masking_number.md)
- [행렬의 덧셈](https://github.com/HK-An/today_i_learned/blob/main/05_CODING/programmers/lv1/sum_of_arrays.md)
- [x만큼 간격이 있는 n개의 숫자](https://github.com/HK-An/today_i_learned/blob/main/05_CODING/programmers/lv1/gap_numbers.md)
- [직사각형 별찍기](https://github.com/HK-An/today_i_learned/blob/main/05_CODING/programmers/lv1/stars.md)
- [완주하지 못한 선수](https://github.com/HK-An/today_i_learned/blob/main/05_CODING/programmers/lv1/retired_participant.md)
</details>

<details>
  <summary>Lv2</summary>

- [문자열압축](https://github.com/HK-An/today_i_learned/blob/main/ALGORITHM/practice/programmers/lv2/string_compression.md)
- [124 나라의 숫자](https://github.com/HK-An/today_i_learned/blob/main/05_CODING/programmers/lv2/weird_number.md)
- [2 x n 타일링](https://github.com/HK-An/today_i_learned/blob/main/05_CODING/programmers/lv2/tile.md)
- [올바른 괄호](https://github.com/HK-An/today_i_learned/blob/main/05_CODING/programmers/lv2/bracket.md)
- [멀쩡한 사각형](https://github.com/HK-An/today_i_learned/blob/main/05_CODING/programmers/lv2/grid.md)
- [기능개발](https://github.com/HK-An/today_i_learned/blob/main/05_CODING/programmers/lv2/release.md)
- [타겟 넘버](https://github.com/HK-An/today_i_learned/blob/main/05_CODING/programmers/lv2/target_number.md)
- [더 맵게](https://github.com/HK-An/today_i_learned/blob/main/05_CODING/programmers/lv2/scoville.md)
- [소수 찾기](https://github.com/HK-An/today_i_learned/blob/main/05_CODING/programmers/lv2/prime_number.md)
- [전화번호 목록](https://github.com/HK-An/today_i_learned/blob/main/05_CODING/programmers/lv2/phone_book.md)
- [짝지어 제거하기](https://github.com/HK-An/today_i_learned/blob/main/05_CODING/programmers/lv2/pair.md)
- [가장 큰 수](https://github.com/HK-An/today_i_learned/blob/main/05_CODING/programmers/lv2/biggest_number.md)
- [프린터](https://github.com/HK-An/today_i_learned/blob/main/05_CODING/programmers/lv2/printer.md)
- [변장](https://github.com/HK-An/today_i_learned/blob/main/05_CODING/programmers/lv2/disguise.md)

</details>

<hr />

#### 백준
지금까지 푼 문제 : **101**문제  
conner@[solved.ac](solved.ac)

<details>
  <summary>1xxx</summary>


- [1000번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p1xxx/P1000.java)
- [1001번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p1xxx/P1001.java)
- [1008번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p1xxx/P1008.java)
- [1018번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p1xxx/P1018.java)
- [1085번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p1xxx/P1085.java)
- [1110번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p1xxx/P1110.java)
- [1152번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p1xxx/P1152.java)
- [1157번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p1xxx/P1157.java)
- [1181번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p1xxx/P1181.java)
- [1197번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p1xxx/P1197.java)
- [1259번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p1xxx/P1259.java)
- [1330번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p1xxx/P1330.java)
- [1436번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p1xxx/P1436.java)
- [1546번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p1xxx/P1546.java)
- [1920번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p1xxx/P1920.java)
- [1926번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p1xxx/P1926.java)
- [1929번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p1xxx/P1929.java)
- [1978번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p1xxx/P1978.java)
</details>

<details>
  <summary>2xxx</summary>

  - [2003번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p2xxx/P2003.java)
  - [2163번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p2xxx/P2163.java)
  - [2231번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p2xxx/P2231.java)
  - [2292번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p2xxx/P2292.java)
  - [2420번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p2xxx/P2420.java)
  - [2438번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p2xxx/P2438.java)
  - [2439번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p2xxx/P2439.java)
  - [2475번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p2xxx/P2475.java)
  - [2480번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p2xxx/P2480.java)
  - [2525번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p2xxx/P2525.java)
  - [2557번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p2xxx/P2557.java)
  - [2559번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p2xxx/P2559.java)
  - [2562번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p2xxx/P2562.java)
  - [2577번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p2xxx/P2577.java)
  - [2588번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p2xxx/P2588.java)
  - [2606번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p2xxx/P2606.java)
  - [2609번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p2xxx/P2609.java)
  - [2675번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p2xxx/P2675.java)
  - [2738번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p2xxx/P2738.java)
  - [2739번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p2xxx/P2739.java)
  - [2741번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p2xxx/P2741.java)
  - [2742번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p2xxx/P2742.java)
  - [2744번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p2xxx/P2744.java)
  - [2751번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p2xxx/P2751.java)
  - [2753번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p2xxx/P2753.java)
  - [2754번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p2xxx/P2754.java)
  - [2798번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p2xxx/P2798.java)
  - [2839번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p2xxx/P2839.java)  
  - [2869번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p2xxx/P2869.java)
  - [2884번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p2xxx/P2884.java)
  - [2908번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p2xxx/P2908.java)
  - [2920번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p2xxx/P2920.java)

</details>

<details>
  <summary>3xxx</summary>

  - [3052번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p3xxx/P3052.java)

</details>

<details>
  <summary>4xxx</summary>

  - [4153번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p4xxx/P4153.java)

</details>

<details>
  <summary>5xxx</summary>

  - [5597번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p5xxx/P5597.java)

</details>

<details>
  <summary>7xxx</summary>

  - [7287번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p7xxx/P7287.java)

</details>

<details>
  <summary>8xxx</summary>

  - [8393번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p8xxx/P8393.java)
  - [8958번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p8xxx/P8958.java)

</details>

<details>
  <summary>9xxx</summary>

  - [9012번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p9xxx/P9012.java)
  - [9086번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p9xxx/P9086.java)
  - [9498번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p9xxx/P9498.java)

</details>

<details>
  <summary>10xxx</summary>

  - [10171번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p10xxx/P10171.java)
  - [10172번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p10xxx/P10172.java)
  - [10250번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p10xxx/P10250.java)
  - [10430번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p10xxx/P10430.java)
  - [10699번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p10xxx/P10699.java)
  - [10718번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p10xxx/P10718.java)
  - [10807번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p10xxx/P10807.java)
  - [10809번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p10xxx/P10809.java)
  - [10814번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p10xxx/P10814.java)
  - [10816번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p10xxx/P10816.java)
  - [10818번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p10xxx/P10818.java)
  - [10845번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p10xxx/P10845.java)
  - [10826번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p10xxx/P10826.java)
  - [10866번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p10xxx/P10866.java)
  - [10869번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p10xxx/P10869.java)
  - [10870번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p10xxx/P10870.java)
  - [10871번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p10xxx/P10871.java)
  - [10872번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p10xxx/P10872.java)
  - [10926번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p10xxx/P10926.java)
  - [10950번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p10xxx/P10950.java)
  - [10951번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p10xxx/P10951.java)
  - [10952번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p10xxx/P10952.java)
  - [10989번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p10xxx/P10989.java)
  - [10998번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p10xxx/P10998.java)

</details>

<details>
  <summary>11xxx</summary>

  - [11021번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p11xxx/P11021.java)
  - [11022번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p11xxx/P11022.java)
  - [11047번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p11xxx/P11047.java)
  - [11050번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p11xxx/P11050.java)
  - [11382번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p11xxx/P11382.java)
  - [11650번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p11xxx/P11650.java)
  - [11654번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p11xxx/P11654.java)
  - [11718번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p11xxx/P11718.java)
  - [11720번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p11xxx/P11720.java)
  - [11726번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p11xxx/P11726.java)
  - [11866번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p11xxx/P11866.java)

</details>

<details>
  <summary>14xxx</summary>

  - [14681번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p14xxx/P14681.java)

</details>

<details>
  <summary>15xxx</summary>

  - [15552번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p15xxx/P15552.java)
  - [15649번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p15xxx/P15649.java)
  - [15650번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p15xxx/P15650.java)
  - [15829번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p15xxx/P15829.java)
  - [15964번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p15xxx/P15964.java)

</details>

<details>
  <summary>16xxx</summary>

  - [16173번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p16xxx/P16173.java)

</details>

<details>
  <summary>18xxx</summary>

  - [18108번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p18xxx/P18108.java)

</details>

<details>
  <summary>25xxx</summary>

  - [25083번](https://github.com/HK-An/coding_practice/blob/main/CodingPractice/baekjoon/src/main/java/kr/hk/p25xxx/P25083.java)

</details>
