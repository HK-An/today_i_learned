# 유클리드 호제법 (Euclidean Algorithm)
###### 작성일: 2022년 07월 01일
## 개요
`유클리드 호제법`은 두 양의 정수의 최대공약수를 구하는 수학적 알고리즘이다.

## 정의
> 두 양의 정수 a, b(a > b)에 대하여 a = bq + r(0 <= r < b)이면, a, b는 최대공약수는 b, r의 최대공약수와 같다.  
> r = 0이라면, a, b의 최대공약수는 b가 된다.

## 활용
위의 정의를 활용하여 다음과 같은 방식으로 최대공약수 및 최소공배수를 구할수 있다.
- 144와 72의 최대공약수 구하기  
> 1444 = 72 * 20 + 4  
> 72 = 4 * 18  
> **gcd(1444, 72) = 4**

- 1444와 72의 최소공배수 구하기  
> 위의 내용에서 이어짐  
> **lcm(1444, 72) = 1444 * 72 / gcd(1444, 72) = 25992**

## 구현코드
https://github.com/HK-An/coding_practice/blob/main/CodingPractice/math/src/main/java/kr/hk/number/EuclideanAlgorithm.java
