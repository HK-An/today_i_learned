# java.util.*

## 개요
자바 기본 라이브러리는 생각보다 많은 기능을 지원한다.
하지만, 어떠한 기능이 구현되어있는지 알지 못하여 해당 기능을 직접 구현하는 경우도 생각보다 빈번하다.
이러한 상황을 방지하기 위하여 여러 발견한 기능을 간단한 예제와 함께 정리하려고 한다.

### Arrays
#### Arrays.copyOfRange(array, int from, int to)
- 첫 번째 파라미터의 `array` 배열을 `from` 인덱스부터 `to` 인덱스의 이전까지 복사하여 리턴한다.
- 파라미터
  1. `array`: 복사하고자 하는 대상이 되는 배열
  2. `from`: 배열에서 복사를 시작하고자 하는 요소의 인덱스
  3. `to`: 배열에서 마지막으로 복사하고자 하는 배열 요소의 **인덱스 + 1**

```java
@Test
    public void test() {
        int[] arrayaa = {1, 2, 3, 4, 5, 6, 7};
        int[] expected = {2, 3, 4, 5};

        int[] usingApi = Arrays.copyOfRange(arrayaa, 1, 4 + 1);
        int[] usingLoop = loop(arrayaa, 1, 4);

        assertThat(usingApi).isEqualTo(expected);
        assertThat(usingLoop).isEqualTo(expected);
        assertThat(usingApi).isEqualTo(usingLoop);
    }

    private int[] loop(int[] array, int start, int end) {
        List<Integer> splitedNumList = new ArrayList<Integer>();
        for(int i = 0; i < array.length; i++) {
            if(i >= start && i <= end) splitedNumList.add(array[i]);
        }
        return splitedNumList.stream().mapToInt(Integer::intValue).toArray();
    }
```
