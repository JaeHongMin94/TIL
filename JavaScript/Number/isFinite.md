# Number.isFinite()

Number.isFinite() 메서드는 인수로 전달된 값이 유한수인지 판별합니다. 판별한 값은 Boolean타입으로 반환합니다.
```javascript
console.log(Number.isFinite(123));  // true
console.log(Number.isFinite(-123)); // true
console.log(Number.isFinite(0));    // true

console.log(isFinite('abc'));       // false
console.log(isFinite(Infinity));    // false - Infinity는 무한수이기 때문에 false입니다.
console.log(isFinite(undefined));   // false
```

## 빌트인 전역 함수

isFinite() 메서드와 Number.isFinite() 메서드는 차이가 있다.
- isFinite() : 인수로 전달된 값이 암묵적 타입 변환이 일어납니다.
- Number.isFinite() : 인수로 전달된 값이 암묵적 타입 변환을 하지 않습니다.
```javascript
console.log(isFinite(null));        // true

console.log(Number.isFinite(null)); // false
```
