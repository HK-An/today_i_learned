# JAVASCRIPT

## 목차


[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## 자바스크립트
### 특징
자바스크립트는 동적 프로토타입 기반 객체지향 언어이며, 싱글스레드기반 논블로킹 비동기처리를 한다.

### 프로토타입
프로토타입 기반 언어는 클래스가 없고 객체 prototype의 위임 과정을 통해 상속의 과정이 구현된다.

### 자바스크립트 엔진의 구조
1. **호출스택**  
자바스크립트는 단 하나의 호출 스택(call stack)을 사용하며 하나의 함수가 실행되면 해당 함수가 끝날때까지 다른 task는 수행할 수 없다는 특징을 지닌다. 메소드가 실행될 때, Call stack에 새로운 프레임이 생기고 push 된 후 실행이 끝나면 해당 프레임은 pop된다.
2. **heap**  
동적으로 생성된 객체는 힙에 할당된다.
3. **Task Queue**  
task queue에서는 처리해야 하는 task들을 임시 저장하는 대기 큐가 존재하며, call stack이 비워졌을 때, 대기열에 들어온 순서대로 실행한다.

### Event Loop
이벤트 루프는 task가 들어오길 기다렸다가 task가 생기면 이를 처리하고 없는 경우에는 잠드는 끊임없이 돌아가는 자바스크립트 내의 루프이다.


[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## ES6
1. **`var` vs `let` vs `const`**  
`var`은 함수 단위의 스코프를 지니지만, `let`과 `const`는 블럭 단위의 스코프를 지닌다.  
`var`은 hoisting 되지만 `let`과 `const`는 hoisting 되지 않는다.
3. **Template Literals 추가**  
\`\`과 ${}의 조합을 사용하여 문자열을 더욱 간단하게 사용할 수 있다.
> const name = 'John Doe'  
const str1 = 'My name is ' + name + '. nice to meet you'  
const str2 = \`My name is ${name}. nice to meet you\`

4. **Arrow Function의 추가**
5. **Maps 추가**


[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## this
1. 기본적으로는 window이다.
2. 메소드의 안: 해당 메소드를 호출한 객체
3. 이벤트 핸들러: 해당 이벤트를 받는 HTML 요소
4. 생성자: 함수가 생성하는 객체
5. 화살표 함수: 해당 함수의 바깥 함수나 클래스의 `this`
6. 명시적 바인딩: 바인딩 해준 객체로 변환.  
`.call(this, a, b)`은 인수 목록을 받고 `.apply(this, [a,b])`는 인수 배열을 받는다.

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## promise, async, await
비동기 코드를 작성하는 새로운 방법이다. Javascript 개발자들이 훌륭한 비동기 처리 방안이 Promise로 만족하지 못하고 더 훌륭한 방법을 고안 해낸 것이다(사실 async/await는 promise기반). 절차적 언어에서 작성하는 코드와 같이 사용법도 간단하고 이해하기도 쉽다. function 키워드 앞에 async를 붙여주면 되고 function 내부의 promise를 반환하는 비동기 처리 함수 앞에 await를 붙여주기만 하면 된다. async/await의 가장 큰 장점은 Promise보다 비동기 코드의 겉모습을 더 깔끔하게 한다는 것이다. 이 것은 es8의 공식 스펙이며 node8LTS에서 지원된다(바벨이 async/await를 지원해서 곧바로 쓸수 있다고 한다!).

Javascript 에서는 대부분의 작업들이 비동기로 이루어진다. 콜백 함수로 처리하면 되는 문제였지만 요즘에는 프론트엔드의 규모가 커지면서 코드의 복잡도가 높아지는 상황이 발생하였다. 이러면서 콜백이 중첩되는 경우가 따라서 발생하였고, 이를 해결할 방안으로 등장한 것이 Promise 패턴이다. Promise 패턴을 사용하면 비동기 작업들을 순차적으로 진행하거나, 병렬로 진행하는 등의 컨트롤이 보다 수월해진다. 또한 예외처리에 대한 구조가 존재하기 때문에 오류 처리 등에 대해 보다 가시적으로 관리할 수 있다. 이 Promise 패턴은 ECMAScript6 스펙에 정식으로 포함되었다.

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## Arrow function
화살표 함수 표현식은 기존의 function 표현방식보다 간결하게 함수를 표현할 수 있다. 화살표 함수는 항상 익명이며, 자신의 this, arguments, super 그리고 new.target을 바인딩하지 않는다. 그래서 생성자로는 사용할 수 없다.
화살표 함수 도입 영향: 짧은 함수, 상위 스코프 this

## null과 undefined의 차이

## ==와 ===의 차이
