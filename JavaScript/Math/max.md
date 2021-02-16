# Math.max()

Math.max() 메서드는 전달된 인수 중에서 가장 큰 수를 반환합니다. 인수가 전달되지 않으면 -Infinity를 반환합니다.
```javascript
console.log(Math.max());           // -Infinity
console.log(Math.max(3));          // 3
console.log(Math.max(4, 3, 1, 2)); // 4
```

배열의 요소 중에서 큰 값을 반환하고 싶다면 Function.prototype.apply 메서드 또는 ES6 스프레드 문법을 사용하면 됩니다.
```javascript
console.log(Math.max.apply(null, [4, 3, 1, 2])); // 4
console.log(Math.max(...[1, 2, 3, 4, 5]));       // 5
```
