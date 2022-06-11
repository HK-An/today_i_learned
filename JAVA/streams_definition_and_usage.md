# JAVA Stream
###### 작성일 : 2022년 06월 08일

## 개요
Stream은 Java 8에 추가되었으며, Lamda를 통하여 for 혹은 foreach 문을 대신할 수 있다. 이를 통하여, 코드의 가독성 및 병렬처리로 인한 성능 개선을 기대할 수 있다. 일반적으로 for(int i=0; ...)과 같은 일반 반복문과 같은 목적으로는 사용하지 않고, for(int num : numList) 과 같은 foreach문을 대체하여 사용하는 편이다.

##  장점
- 코드의 가독성이 좋아진다.
- 간단하고 양이 많은 업무를 병렬로 돌려주어 성능 향상을 기대할 수 있다.
- JAVA에서 함수형 프로그래밍이 가능해진다.
- 원본의 데이터를 변경하지 않는다.

## 단점
- 재사용이 불가능한 일회용 코드이다.
- 병렬에 따른 오버헤드가 발생할 수 있다.

## Stream 사용하기
Streams에 관한 내용은 크게 세 가지로 나눌 수 있다.  
1.  [생성하기](https://github.com/HK-An/today_i_learned/blob/main/JAVA/streams_definition_and_usage.md#%EC%83%9D%EC%84%B1%ED%95%98%EA%B8%B0)
2.  [가공하기](https://github.com/HK-An/today_i_learned/blob/main/JAVA/streams_definition_and_usage.md#%EA%B0%80%EA%B3%B5%ED%95%98%EA%B8%B0)
3.  [결과 만들기](https://github.com/HK-An/today_i_learned/blob/main/JAVA/streams_definition_and_usage.md#%EA%B2%B0%EA%B3%BC-%EB%A7%8C%EB%93%A4%EA%B8%B0)

흐름 : 전체 → mapping → filtering1 → filtering2 → 결과 만들기 → 결과물
<hr>

### 생성하기
Stream을 사용하기 위한 Stream Instance를 생성하는 단계이다. 배열, Collection, 수 또는 파일 등 다양한 종류의 데이터를 가지고 Stream을 생성할 수 있다.

#### 배열 Stream

Stream을 사용하기 위해선 먼저 생성해야한다. Arrays.stream 메소드를 사용하여 Stream에서 배열을 이용할 수 있다.
```java
String[] arr = new String[]{"a", "b", "c"};
Stream<String> stream = Arrays.stream(arr);
Stream<String> streamOfArrayPart =
  Arrays.stream(arr, 1, 3); // 1~2 요소 [b, c]
```
#### 컬렉션 Stream
Collection, List, Set 등의 경우 default method `stream`을 사용하여 생성 가능하다.
```java
List<String> list = Arrays.asList("a", "b", "c");
Stream<String> stream = list.stream();
Stream<String> parallelStream = list.parallelStream(); // 병렬 처리 스트림
```
#### 비어 있는 Stream

empty streams는 요소가 없을때 null 대신 사용 가능하다.
```java
public Stream<String> streamOf(List<String> list) {
  return list == null || list.isEmpty()
    ? Stream.empty()
    : list.stream();
}
```
#### Stream.builder()
Builder를 사용 시 Stream에 원하는 값을 직접 넣을 수 있다.
```java
Stream<String> builderStream =
  Stream.<String>builder()
    .add("Eric").add("Elena").add("Java")
    .build(); // [Eric, Elena, Java]
```
#### Stream.iterate()
초기값과 해당 값을 다루는 람다를 이용하여 Streams에 들어갈 요소를 만들 수 있다. 특정 사이즈로 제한이 필요하다.
```java
Stream<Integer> iteratedStream =
  Stream.iterate(30, n -> n + 2).limit(5); // [30, 32, 34, 36, 38]
```
#### 기본 타입형 Stream
```java
IntStream intStream = IntStream.range(1, 5); // [1, 2, 3, 4]
LongStream longStream = LongStream.rangeClosed(1, 5); // [1, 2, 3, 4, 5]
Stream<Integer> boxedIntStream = IntStream.range(1, 5).boxed();
DoubleStream doubles = new Random().doubles(3); // 난수 3개 생성
IntStream charsStream =
  "Stream".chars(); // [83, 116, 114, 101, 97, 109]
```
##### 문자열 Stream
```java
Stream<String> stringStream =
  Pattern.compile(", ").splitAsStream("Eric, Elena, Java");
  // [Eric, Elena, Java]
```
##### 파일 Stream
```java
Stream<String> lineStream =
  Files.lines(Paths.get("file.txt"),
              Charset.forName("UTF-8"));
```
##### Stream 연결하기

```java
Stream<String> stream1 = Stream.of("Java", "Scala", "Groovy");
Stream<String> stream2 = Stream.of("Python", "Go", "Swift");
Stream<String> concat = Stream.concat(stream1, stream2);
// [Java, Scala, Groovy, Python, Go, Swift]
```
<hr>

### 가공하기

원본 데이터를 원하는 형태의 데이터로 가공하기 위한 연산단계이다. Filtering 및 Mapping등을 통하여 원하는 결과를 결과를 만들어내는 중간 작업이며 이러한 작업은 Stream을 return하기 때문에 여러작업을 이어 붙여서 할 수 있다.
```java
List<String> names = Arrays.asList("Eric", "Elena", "Java");
// 아래부터는 이걸 예제로 활용함
```

#### Filtering
Stream 내의 요소들을 하나씩 평가해서 걸러내는 작업이다.
```java
Stream<String> stream =
  names.stream()
  .filter(name -> name.contains("a"));
// [Elena, Java]
```

#### Mapping
Stream 내 요소들을 하나씩 특정 값으로 변환해준다. Stream에 들어있는 값이 input이 되어 특정 로직을 거친 후 return되는 새로운 Stream에 담기게 된다.
```java
Stream<String> stream =
  names.stream()
  .map(String::toUpperCase);
// [ERIC, ELENA, JAVA]
```

#### FlatMap
중첩 구조를 한단계 제거하고 단일 컬렉션으로 만들어준다.
```java
List<List<String>> list =
  Arrays.asList(Arrays.asList("a"),
                Arrays.asList("b"));
// [[a], [b]]
List<String> flatList =
  list.stream()
  .flatMap(Collection::stream)
  .collect(Collectors.toList());
// [a, b]
```
```java
students.stream()
  .flatMapToInt(student ->
                IntStream.of(student.getKor(),
                             student.getEng(),
                             student.getMath()))
  .average().ifPresent(avg ->
                       System.out.println(Math.round(avg * 10)/10.0));
// 학생 객체를 가진 스트림에서 학생의 국영수 점수를 뽑아
// 새로운 스트림을 만들어 평균을 구하는 코드
```

#### Sorting
1.  인자를 넘기지 않는 경우
```java
IntStream.of(14, 11, 20, 39, 23)
  .sorted()
  .boxed()
  .collect(Collectors.toList());
// [11, 14, 20, 23, 39]
```

2.  인자를 넘기는 경우와 그렇지 않은 경우를 비교

```java
// Case 1
List<String> lang =
  Arrays.asList("Java", "Scala", "Groovy", "Python", "Go", "Swift");

lang.stream()
  .sorted() // 인자가 없어 자동으로 알파벳 순 정렬
  .collect(Collectors.toList());
// [Go, Groovy, Java, Python, Scala, Swift]

lang.stream()
  .sorted(Comparator.reverseOrder()) // Compartor을 사용하여 역순 정렬
  .collect(Collectors.toList());
// [Swift, Scala, Python, Java, Groovy, Go]

// Case 2
lang.stream()
  .sorted(Comparator.comparingInt(String::length)) // Comparator의 길이 비교를 사용
  .collect(Collectors.toList());
// [Go, Java, Scala, Swift, Groovy, Python]

lang.stream()
  .sorted((s1, s2) -> s2.length() - s1.length()) // Compare 메소드 사용
  .collect(Collectors.toList());
// [Groovy, Python, Scala, Swift, Java, Go]
```

#### Iterating
Iterating은 특정 결과를 반환하지 않고 지정한 동작만 수행한다.

```java
int sum = IntStream.of(1, 3, 5, 7, 9)
  .peek(System.out::println)
  .sum();

```
<hr>

### 결과 만들기
가공된 데이터로 원하는 결과를 만들기 위한 최종 연산단계이며 Stream의 요소들을 소모하여 연산하기 때문에 1번만 수행 가능하다.

#### Calculating

Stream이 비어있는 경우 `count`와 `sum`은 0을 출력하면 되지만, `avg`, `max`, `min`의 경우에는 표현할 수 있는 기본값이 없기 때문에 `Optional`을 이용해 return 한다.

```java
long count = IntStream.of(1, 3, 5, 7, 9).count();
long sum = LongStream.of(1, 3, 5, 7, 9).sum();
DoubleStream.of(1.1, 2.2, 3.3, 4.4, 5.5)
  .average()
  .ifPresent(System.out::println);
```

#### Collecting
```java
List<Product> productList =
  Arrays.asList(new Product(23, "potatoes"),
                new Product(14, "orange"),
                new Product(13, "lemon"),
                new Product(23, "bread"),
                new Product(13, "sugar"));
// 아래부턴 이걸 예제로 활용함.
```

##### Collectors.toList()
```java
List<String> collectorCollection =
  productList.stream()
    .map(Product::getName)
    .collect(Collectors.toList());
// [potatoes, orange, lemon, bread, sugar]
```

##### Collectors.joining()
3개의 인자를 받을 수 있다.
-   delimiter : 각 요소 중간에 들어가 요소를 구분시켜주는 구분자
-   prefix : 결과 맨 앞에 붙는 문자
-   suffix : 결과 맨 뒤에 붙는 문자

```java
String listToString =
 productList.stream()
  .map(Product::getName)
  .collect(Collectors.joining());
// potatoesorangelemonbreadsugar

String listToString =
 productList.stream()
  .map(Product::getName)
  .collect(Collectors.joining(", ", "<", ">"));
// <potatoes, orange, lemon, bread, sugar>
```

##### Collectors.averageingInt()
```java
Double averageAmount =
 productList.stream()
  .collect(Collectors.averagingInt(Product::getAmount));
// 17.2
```

##### Collectors.summingInt()
```java
Integer summingAmount =
 productList.stream()
  .collect(Collectors.summingInt(Product::getAmount));
// 86

Integer summingAmount =
  productList.stream()
  .mapToInt(Product::getAmount)
  .sum(); // 86
```

##### Collectors.summarizingInt()

합계와 평균등이 같이 필요할때 사용한다.

-   개수 _getCount()_
-   합계 _getSum()_
-   평균 _getAverage()_
-   최소 _getMin()_
-   최대 _getMax()_
```java
IntSummaryStatistics statistics =
 productList.stream()
  .collect(Collectors.summarizingInt(Product::getAmount));
```

##### Collectors.groupingBy()

결과는 기본적으로 Map타입으로 나오며, 같은 수량일 경우 List로 묶어서 보여준다.

```java
Map<Integer, List<Product>> collectorMapOfLists =
 productList.stream()
  .collect(Collectors.groupingBy(Product::getAmount));

/*
{23=[Product{amount=23, name='potatoes'},
     Product{amount=23, name='bread'}],
 13=[Product{amount=13, name='lemon'},
     Product{amount=13, name='sugar'}],
 14=[Product{amount=14, name='orange'}]}
*/

```

##### Collectors.partitioningBy()
```java
Map<Boolean, List<Product>> mapPartitioned =
  productList.stream()
  .collect(Collectors.partitioningBy(el -> el.getAmount() > 15));

/*
{false=[Product{amount=14, name='orange'},
        Product{amount=13, name='lemon'},
        Product{amount=13, name='sugar'}],
 true=[Product{amount=23, name='potatoes'},
       Product{amount=23, name='bread'}]}
*/

```

##### Collectors.collectingAndThen()

`collect`후에 추가 작업이 필요할 경우에 사용한다.

```java
Set<Product> unmodifiableSet =
 productList.stream()
  .collect(Collectors.collectingAndThen(Collectors.toSet(),
                                        Collections::unmodifiableSet));
```

##### Collector.of()

그 외 필요한 로직이 있을 경우 직접 만들수도 있다.

```java
Collector<Product, ?, LinkedList<Product>> toLinkedList =
  Collector.of(LinkedList::new,
               LinkedList::add,
               (first, second) -> {
                 first.addAll(second);
                 return first;
               });
```

#### Matching
-   하나라도 조건을 만족하는 요소가 있는지(_anyMatch_)
-   모두 조건을 만족하는지(_allMatch_)
-   모두 조건을 만족하지 않는지(_noneMatch_)
```java
List<String> names = Arrays.asList("Eric", "Elena", "Java");

boolean anyMatch = names.stream()
  .anyMatch(name -> name.contains("a")); // true
boolean allMatch = names.stream()
  .allMatch(name -> name.length() > 3); // true
boolean noneMatch = names.stream()
  .noneMatch(name -> name.endsWith("s")); // true
```

#### Iterating

`peek`과는 중간 작업인지 최종 작업인지 정도의 차이를 가지고 있으며 보통 `System.out.println` 메소드를 넘겨서 결과를 출력할 때 사용한다.
<hr>

>출처
> - https://futurecreator.github.io/2018/08/26/java-8-streams/
> - https://okky.kr/article/329818
> - https://mangkyu.tistory.com/112#:~:text=Stream%EC%9D%84%20%EC%9D%B4%EC%9A%A9%ED%95%98%EB%A9%B4%20%EC%BD%94%EB%93%9C,%EC%9D%98%20%EC%9E%91%EC%84%B1%EC%9D%B4%20%EA%B0%80%EB%8A%A5%ED%95%98%EB%8B%A4
