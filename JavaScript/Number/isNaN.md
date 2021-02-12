# Number.isNaN()

Number.isNaN() 메서드는 인수로 전달된 값이 NaN인지 판별합니다. 판별한 값은 Boolean타입으로 반환합니다.
```javascript
console.log(Number.isNaN(NaN));   // true
console.log(Number.isNaN(1));     // false
console.log(Number.isNaN('123')); // false
```

## 빌트인 전역 함수

isNaN() 메서드와 Number.isNaN() 메서드는 차이가 있다.
- isNaN() : 인수로 전달된 값이 암묵적 타입 변환이 일어납니다.
- Number.isNaN() : 인수로 전달된 값이 암묵적 타입 변환을 하지 않습니다.
```javascript
console.log(isNaN(undefined));    // true

console.log(Number.isNaN(undefined));   // false
```
