# JAVASCRIPT

## 목차
1. [자바스크립트](https://github.com/HK-An/today_i_learned/tree/main/02_LANGUAGE/02_JAVASCRIPT#자바스크립트)
    1. [특징](https://github.com/HK-An/today_i_learned/tree/main/02_LANGUAGE/02_JAVASCRIPT#특징)
    1. [프로토타입](https://github.com/HK-An/today_i_learned/tree/main/02_LANGUAGE/02_JAVASCRIPT#프로토타입)
    1. [자바스크립트 엔진의 구조](https://github.com/HK-An/today_i_learned/tree/main/02_LANGUAGE/02_JAVASCRIPT#자바스크립트-엔진의-구조)
    1. [Event Loop](https://github.com/HK-An/today_i_learned/tree/main/02_LANGUAGE/02_JAVASCRIPT#event-loop)
1. [ES6](https://github.com/HK-An/today_i_learned/tree/main/02_LANGUAGE/02_JAVASCRIPT#es6)
1. [this](https://github.com/HK-An/today_i_learned/tree/main/02_LANGUAGE/02_JAVASCRIPT#this)
1. [Promise, Asnyc, Await](https://github.com/HK-An/today_i_learned/tree/main/02_LANGUAGE/02_JAVASCRIPT#promise-async-await)
1. [Arrow Function](https://github.com/HK-An/today_i_learned/tree/main/02_LANGUAGE/02_JAVASCRIPT#arrow-function)
1. [null과 undefined의 차이](https://github.com/HK-An/today_i_learned/tree/main/02_LANGUAGE/02_JAVASCRIPT#null과-undefined의-차이)
1. [==와 ===의 차이](https://github.com/HK-An/today_i_learned/tree/main/02_LANGUAGE/02_JAVASCRIPT#와-의-차이)

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## 자바스크립트
### 특징
자바스크립트는 동적 프로토타입 기반 객체지향 언어이며, 싱글스레드기반 논블로킹 비동기처리를 한다.

### 프로토타입
프로토타입 기반 언어는 클래스가 없고 객체 prototype의 위임 과정을 통해 상속의 과정이 구현된다.

> 자바스크립트는 한마디로 정의하면 동적 프로토타입 기반 객체지향 언어입니다. 자바스크립트는 싱글 스레드 기반 논블로킹 비동기로 동작하며 프로토타입은 class 없이 prototype의 위임 과정을 통해 상속의 과정이 구현되는 것을 의미합니다.

### 자바스크립트 엔진의 구조
1. **호출스택**  
자바스크립트는 단 하나의 호출 스택(call stack)을 사용하며 하나의 함수가 실행되면 해당 함수가 끝날때까지 다른 task는 수행할 수 없다는 특징을 지닌다. 메소드가 실행될 때, Call stack에 새로운 프레임이 생기고 push 된 후 실행이 끝나면 해당 프레임은 pop된다.
2. **heap**  
동적으로 생성된 객체는 힙에 할당된다.
3. **Task Queue**  
task queue에서는 처리해야 하는 task들을 임시 저장하는 대기 큐가 존재하며, call stack이 비워졌을 때, 대기열에 들어온 순서대로 실행한다.

### Event Loop
이벤트 루프는 task가 들어오길 기다렸다가 task가 생기면 이를 처리하고 없는 경우에는 잠드는 끊임없이 돌아가는 자바스크립트 내의 루프이다.

> 자바스크립트 엔진은 호출스택, 힙, 테스크 큐의 3가지로 이루어져있습니다. 먼저 호출스택은 함수 정보등이 저장되는 영역이며, 힙은 사용자가 동적으로 할당하는 영역입니다. 마지막으로 task queue의 경우 처리해야 하는 task를 입시 저장하기 위한 공간으로 호출 스택이 비워졌을 시, 대기열에 들어온 순서대로 실행하게 됩니다.

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
6. **`Promise`의 추가**

> ES6에서는 여러 문법적인 내용이 추가되었는데 let과 const의 변경, 템퍼럴 리터럴 추가, 화살표 함수 추가, map 추가, promise의 추가를 들 수 있습니다.

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

> this는 자바스크립트에서 호출 객체를 의미하는 것으로 몇몇 경우를 제외하고는 window입니다. 예외상황에는 메소드의 안에서는 해당 메소드를 호출한 객체가 되며, 이벤트 핸들러에서는 이벤트를 받는 HTML 요소, 생성자에서는 함수가 생성하는 객체, 화살표 함수는 해당 함수의 바깥 함수나, 클래스의 this의 상태를 지닙니다.

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## promise, async, await
1.  Promise  
`Promise`는 비동기 작업의 단위로서 콜백 지옥을 해결하기 위한 방안으로 등장하였다. `Promise`는 "new Promise(..)"로 선언하는 순간부터 시작되며, `.then()`이나 `.catch()`를 사용하여 후속 동작을 지정해주어야 한다.

2. Async/Await  
`Async`는 함수를 선언할때 사용되며 함수 앞에 `async` 키워드를 붙여주면 비동기 함수로 선언할 수 있다. `async`를 사용하여 만든 비동기 함수는 항상 `Promise`를 리턴한다. `Await`는 `asnyc`로 선언한 함수의 값을 기다려서 값을 받아오기 위한 방법이며 `await` 키워드는 async 함수 안에서만 동작한다.

> Promise와 Async/Await 모두 비동기 작업을 처리하기 위해서 사용하는 기술인데요. 두가지 방법의 차이는 에러 헨들링과 코드 가독성이 있습니다. Promise는 .catch() 메소드로 바로 에러 처리가 가능하지만, async/await은 try-catch문을 사용하여야 합니다. 또, Promise는 코드가 길어질수록 복잡해질 수 있는 가능성이 있고 .then() 지옥에 빠질 수 있지만 async/await은 보다 코드 흐름을 이해하기 쉽습니다.

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## Arrow function
화살표 함수 표현식은 기존의 function 표현방식보다 간결하게 함수를 표현할 수 있다. 화살표 함수는 항상 익명이며, 자신의 this, arguments, super 그리고 new.target을 바인딩하지 않는다. 그래서 생성자로는 사용할 수 없다.

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## null과 undefined의 차이
undefined는 변수를 선언하고 값을 할당하지 않은 상태 즉, 자료형이 없는 상태이고, null은 변수를 선언하고 빈 값을 할당한 상태이다.

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## ==와 ===의 차이
==은 Equal Operator이고, ===은 Strict Operator이다. 이 둘의 차이는 Equal Operator는 그저 값만 비교하고 Strict Operator는 값과 데이터 타입을 같이 비교하는 것에 있다.

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />
