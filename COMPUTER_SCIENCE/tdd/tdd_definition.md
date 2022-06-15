## 개요

테스트 주도 개발(TDD)이란 매우 짧은 개발 사이클을 반복하는 소프트웨어 개발 프로세스 중 하나이다.  
개발자는 요구사항을 검증하는 자동화된 테스트 케이스를 만들고 이 테스트 케이스를 통과하기 위한 최소한의 코드를 작성한다.

## TDD 개발 주기

![](https://velog.velcdn.com/images/hk_an/post/f1b27845-25f0-4bcb-9c67-306f14350b5d/image.png)  
TDD의 개발은 위의 그림에서의 Red, Green, Refactor의 3가지 주기로 이루어진다.

### Red

이 단계에서는 테스트에 통과하지 못하는 코드를 작성한다.

```java
=============
TEST CODE
=============
@Test
public void test_getAvg() {
	// given
    int[] numArr = [2, 3, 7];
    // when
    int answer = getAvg(numArr);
    
    // then
    assertThat(answer).isEqualTo(4);
}
=============
public int getAvg(int[] numArr) {
	return numArr[0]-1;
}

```

### Green

이 단계에서는 테스트에 통과하는 코드를 작성한다.

```java
=============
TEST CODE 생략
=============

public int getAvg(int[] numArr) {
	int result = 0;
    int size = numArr.length;
    int sum = 0;
    
    for(int i = 0; i < size; i++) {
    	sum += numArr[i];
    }
    
    result = sum / size;
    
	return result;
}

```

### Refactor

이 단계에서는 중복코드 제거 등의 클린코드를 위한 작업을 수행한다.

```java
=============
...
@Test
public void test_getSum() {
 ...
}

=============

public int getAvg(int[] numArr) {
	int result = 0;
    int size = numArr.length;
    int sum = getSum(numArr);
    
    result = sum / size;
    
	return result;
}

private int getSum(int[] numArr) {
    int sum = 0;

	for(int i = 0; i < size; i++) {
    	sum += numArr[i];
    }
    
    return sum;
}
```

## TDD의 장점

### 1. 코드의 유지보수성이 향상됨

자동화된 테스트로 인하여 디버깅 시간이 단축되고, 사람이 눈으로 직접 확인해가며 테스트 하는 것보다 실수할 가능성이 줄어든다. 이렇게 되면 새로운 기능을 추가하거나 기능을 수정할 당시 깨닫지 못하는 영향(다른 곳에서 수정한 메소드를 사용하는 등)을 미리 확인할 수 있다.

### 2. 문서화에 들어가는 시간 단축

테스트 코드 자체가 수행되는 코드의 훌륭한 문서이므로 문서화에 들이는 시간이 매우 단축될 수 있다.