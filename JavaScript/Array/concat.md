# Array.prototype.concat()

concat() 메서드는 인수로 전달받은 값을 배열 마지막 요소에 추가합니다. **원본 배열은 변경되지 않습니다.**

## 사용 예시

```javascript
const arr = [1, 2, 3];
const result = arr.concat(4);

console.log(result); // [ 1, 2, 3, 4 ]
console.log(arr);    // [ 1, 2, 3 ]
```

### concat() 메서드의 특징

concat() 메서드는 전달 받은 인수가 배열이라면 해체한 후에 배열의 마지막 요소로 추가합니다.

```javascript
const arr = [1, 2, 3];
const result = arr.concat([4, 5]);

console.log(result); // [ 1, 2, 3, 4, 5 ]
console.log(arr);    // [ 1, 2, 3 ]
```

- 비슷한 메서드 push()는 해체하지 않고 그대로 배열 마지막 요소에 추가합니다.

```javascript
const arr = [1, 2, 3];
arr.push([4, 5]);

console.log(arr); // [ 1, 2, 3, [ 4, 5 ] ]
```

### ES6에 추가된 스프레드 문법

concat() 메서드는 ES6에 추가된 스프레드 문법으로 대체할 수 있습니다.

```javascript
const arr = [1, 2, 3];
const result = arr.concat([4, 5]);
const result2 = [...arr, 4, 5];

console.log(result);  // [ 1, 2, 3, 4, 5 ]
console.log(result2); // [ 1, 2, 3, 4, 5 ]
console.log(arr);     // [ 1, 2, 3 ]
```

