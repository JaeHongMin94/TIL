# Math.abs()

Math.abs() 메서드는 인수로 전달된 값을 절대값으로 반환합니다.
```javascript
console.log(Math.abs(-1));        // 1
console.log(Math.abs('-1'));      // 1
console.log(Math.abs(''));        // 0
console.log(Math.abs([]));        // 0
console.log(Math.abs(null));      // 0
console.log(Math.abs(undefined)); // NaN
console.log(Math.abs({}));        // NaN
console.log(Math.abs('string'));  // NaN
console.log(Math.abs());          // NaN
```
