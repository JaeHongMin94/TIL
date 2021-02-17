# Array.prototype.indexOf()

Array.prototype.indexOf() 메서드는 배열안에 특정 요소가 있는지 확인하고 존재한다면 요소의 위치를 반환합니다.<br />
요소가 존재하지 않다면 -1을 반환합니다.

```javascript
const arr = [1, 2, 3, 4, 4, 5];

console.log(arr.indexOf(2)); // 1
console.log(arr.indexOf(4)); // 3
console.log(arr.indexOf(6)); // -1
```
