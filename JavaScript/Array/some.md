# Array.prototype.some()

Array.prototype.some() 메서드는 배열의 요소 중 콜백 함수의 반환값을 판별해서 true, false를 반환합니다.

- 값이 하나라도 true라면 true를 반환합니다. 논리 연산자 or와 같습니다.
- 모든 값이 false일 경우에만 false를 반환합니다.
- 원본 배열 값을 변경되지 않습니다.

```js
const arr = [2, 4, 8, 16, 32];

console.log(arr.some((element) => element > 30)); // true
console.log(arr.some((element) => element < 2));  // false
console.log([].some((element) => element > 20));  // false - 빈 배열([])은 false를 반환합니다.
```
