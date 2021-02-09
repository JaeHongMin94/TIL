# Array.prototype.slice()

slice() 메서드는 배열의 처음부터 끝가지 원하는 요소들을 복사하여 배열로 반환합니다. **단, 원본 배열을 변경되지 않습니다.**

## slice() 메서드의 2가지 매개변수

> slice(start, end)

- start : 복사를 시작할 배열의 index 위치를 지정합니다.
- end : 복사를 종료할 배열의 index 위치를 지정합니다. 지정한 index 전까지만 복사합니다. 생략할 경우 끝까지 복사합니다.
  - slice(3, 5) : arr[3]부터 arr[5]이전의 요소까지만 복사합니다.
  
## 사용예시
```javascript
const arr = [1, 2, 3, 4, 5, 6, 7];
const result = arr.slice(3, 5);

console.log(arr.slice(3, 5)); // [ 4, 5 ]
console.log(result);          // [ 4, 5 ]
console.log(arr);             // [ 1, 2, 3, 4, 5, 6, 7 ]
```
- slice() 메서드는 원본 배열이 변경되지 않기 때문에 값을 보관하고 싶다면 새로운 변수를 만들어서 할당해야 합니다.

## end 매개변수를 생략했을 경우
```javascript
const arr = [1, 2, 3, 4, 5, 6, 7];
const result = arr.slice(3);

console.log(arr.slice(3)); // [ 4, 5, 6, 7 ]
console.log(result);       // [ 4, 5, 6, 7 ]
console.log(arr);          // [ 1, 2, 3, 4, 5, 6, 7 ]
```
- 생략할 경우 index 시작 위치부터 끝가지 복사합니다.
