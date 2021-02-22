# Array.prototype.every()

Array.prototype.every() 메서드는 배열의 요소 중 콜백 함수의 반환값을 판별해서 true, false를 반환합니다.

- 값이 하나라도 false라면 false를 반환합니다. 논리 연산자 and와 같습니다.
- 모든 값이 true일 경우에만 true를 반환합니다.
- 원본 배열 값을 변경되지 않습니다.

```js
const arr = [2, 4, 8, 16, 32];

console.log(arr.every((element) => element > 30)); // false
console.log(arr.every((element) => element < 2));  // false
console.log(arr.every((element) => element > 1));  // true
console.log([].every((element) => element > 20));  // true - 빈 배열([])은 true를 반환합니다.
```
