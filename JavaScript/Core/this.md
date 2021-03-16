# this

JavaScript에서 가장 혼란스러운 개념중에 하나인 this입니다. this의 값은 함수를 호출하는 방법에 의해 결정됩니다.<br>

## 상황에 따라 달라지는 this

this는 실행 컨텍스트가 생성될 때 함께 결정되고, 함수를 호출할 때 결정됩니다. 또한 함수를 어떤 방식으로 호출하느냐에 따라 값이 달라지는 것입니다.

### 전역 공간에서의 this

``` js
var num = 1;
console.log(num);         // 1
console.log(window.num);  // 1
console.log(this.num);    // 1

window.num = 2;
console.log(num);         // 2
console.log(window.num);  // 2
console.log(this.num);    // 2
```
전역 공간에서의 this는 **전역변수를 선언하면 자바스크립트 엔진은 이를 전역객체의 프로퍼티로 할당합니다.**<br>

```js
var book = 'JS';
console.log(this.book);  // JS

function whatBook() {
this.book2 = 'Java';
console.log(this);
}

console.log(this.book);  // JS
console.log(this.book2); // undefined

window.book = 'C';

console.log(this.book);  // C
console.log(this.book2); // undefined

whatBook();              // window

console.log(this.book);  // C
console.log(this.book2); // Java
```
여기서 알 수 있는 점은 일반 함수로 호출하면 함수 내부의 this는 전역 객체로 바인딩하는 것을 알 수 있다.<br>
하지만 'use strict'모드(엄격한 모드)를 적용하게되면 일반 함수 내부의 this는 undefinde가 바인딩됩니다.

```js
function foo() {
  'use strict';

  console.log("foo's this: ", this);
  function bar() {
    console.log("bar's this: ", this);
  }
  bar(); // undefined
}

foo();   // undefined
```
<br>
다음으로 살펴볼 것은 메서드 내에서 정의한 중첩 함수도 일반 함수로 호출되면 중첩 함수 내부의 this도 전역 객체로 바인딩 되는가이다.

```js
var book = 'JS';

const list = {
  book: 'Java',
  foo() {
    console.log("foo's this: ", this);
    console.log("foo's this.book: ", this.book);

    function bar() {
      console.log("bar's this: ", this);
      console.log("bar's this.book: ", this.book);
    }

    bar();
  },
};

list.foo();
```
위와 같이 this는 어떠한 함수라도 일반 함수로 호출되면 전역 객체가 바인딩됩니다.
