# Number.prototype.toExponential()

Number.prototype.toExponential() 메서드는 숫자를 지수 표기법으로 변환 후 문자열로 반환합니다.
- 메서드안에 값은 소수점 이하로 표현할 자릿수입니다. 기본값은 주어진 값을 나타내는데 필요한 자릿수입니다.

## Example
```javascript
console.log((1234).toExponential());   // 1.234e+3
console.log((1.234).toExponential(2)); // 1.23e+0
console.log((1.234).toExponential(4)); // 1.2340e+0
```

## 주의사항

숫자뒤에 .toExponential()을 쓰는 것을 조심해야한다. <br />
```javascript
console.log(1234.toExponential()) // SyntaxError: Invalid or unexpected token
```

JavaScript 엔진은 숫자 뒤에 .을 부동 소수점 구분기호로 해석하기 떄문입니다. 이를 해결할 수 있는 방법은 .앞에 공백 한칸을 만드는 것이다. <br />
```javascript
console.log(123 .toExponential()) // 1.23e+2 
```

실수뒤에 .toExponential()을 사용하는 것은 가능합니다. 두번째 .은 프로퍼티 접근 연산자로 해석하기 때문입니다.
```javascript
console.log(1.23.toExponential()); // 1.23e+0
```

권장하는 방법은 그룹연산자를 사용하는 것입니다.
```javascript
console.log((1.234).toExponential()); // 1.234e+0
```
