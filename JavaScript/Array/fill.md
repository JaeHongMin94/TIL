# Array.prototype.fill()

Array.prototype.fill() 메서드는 인수로 전달된 값을 배열의 처음부터 끝까지 요소로 채웁니다. **원본 배열이 변경됩니다.**

## fill() 메서드의 3가지 매개변수

> fill(value, start, end)

- value : 배열을 채울 값
- start : 시작 인덱스, end에 값을 넣지 않을 경우 배열의 끝까지 채워집니다.
- end : 끝 인덱스, ex) 3일 경우 이전의 인덱스까지 채워집니다.

## Example
```javascript
const arr = [1, 2, 3, 4, 4, 5];
const arr2 = [1, 2, 3, 4, 4, 5];
const arr3 = [1, 2, 3, 4, 4, 5];

console.log(arr.fill(7));        // [ 7, 7, 7, 7, 7, 7 ]
console.log(arr2.fill(8, 1));    // [ 1, 8, 8, 8, 8, 8 ]
console.log(arr3.fill(9, 1, 4)); // [ 1, 9, 9, 9, 4, 5 ]
```
