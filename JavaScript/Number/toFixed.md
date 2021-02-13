# Number.prototype.toFixed()

Number.prototype.toFixed() 메서드는 숫자를 반올림해서 문자열로 반환합니다.
 - 전달된 인수는 소수점의 자릿수를 나타냅니다.
 - 기본값은 0입니다.
 
## Example
```javascript
console.log((123.4567).toFixed());                                // 123
console.log((123.4567).toFixed(2));                               // 123.46
console.log((123.4567).toFixed(4), typeof (123.4567).toFixed(4)); // 123.4567 string
```
