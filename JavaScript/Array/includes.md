# Array.prototype.includes()

Array.prototype.includes() 메서드는 배열 내에 요소가 존재하는지 판별합니다.

## includes() 메서드의 매개변수

> includes(value, start)

- value : 배열안에서 찾을 요소 값
- start : 요소 검사를 시작할 위치, 기본값은 0입니다.

```javascript
const arr = [1, 2, 3, 4, 5];

console.log(arr.includes(2));     // true
console.log(arr.includes(2, 2));  // false
console.log(arr.includes(3, -3)); // true
```
