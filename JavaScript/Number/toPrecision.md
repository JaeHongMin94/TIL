# Number.prototype.toPrecision()

Number.prototype.toPrecision() 메서드는 전체 자릿수까지 유효하도록 나머지 자릿수를 반올림하여 문자열로 반환합니다.
- 인수로 전달받은 전체 자릿수로 표현할 수 없는 경우 지수 표기법으로 결과를 반환합니다.
- 기본값은 0으로 지정됩니다.

## Example
```javascript
console.log((123.4567).toPrecision());                              // 123.4567
console.log((123.4567).toPrecision(2));                             // 1.2e+2
console.log((123.4).toPrecision(5), typeof (123.4).toPrecision(5)); // 123.40 string
```
