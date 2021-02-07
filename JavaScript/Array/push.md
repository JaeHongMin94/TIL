# Array.prototype.push()

push() 메서드는 배열끝에 요소들을 하나이상 추가한다. **원본 배열을 직접 변경**한다.

## 사용 예시
```javascript
const arr = [1, 2, 3];

arr.push(4);
console.log(arr); // [ 1, 2, 3, 4 ]

arr.push(5, 6);
console.log(arr); // [ 1, 2, 3, 4, 5, 6 ]
```
