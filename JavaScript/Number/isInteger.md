# Number.isInteger()

Number.isInteger() 메서드는 인수로 전달된 값이 정수인지 판별합니다. 판별한 값은 Boolean타입으로 반환합니다.
```javascript
console.log(Number.isInteger(0));         // true
console.log(Number.isInteger(1));         // true
console.log(Number.isInteger(-1));        // true

console.log(Number.isInteger(0.1));       // false
console.log(Number.isInteger('123'));     // false
console.log(Number.isInteger(NaN));       // false
console.log(Number.isInteger(undefined)); // false
```
