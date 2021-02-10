# Array.prototype.join()

join() 메서드는 배열의 모든 요소를 문자열로 반환합니다.<br />
문자열은 구분자로 연결되어 반환합니다.<br />
구분자는 생략가능하며 기본값은 콤마(,) 입니다.

## 사용 예시
```javascript
const arr = [1, 2, 3, 4, 5];

console.log(arr.join());    // 1,2,3,4,5
console.log(arr.join(''));  // 12345
console.log(arr.join(' ')); // 1 2 3 4 5
```
