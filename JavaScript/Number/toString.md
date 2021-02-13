# Number.prototype.toString()

Number.prototype.toString() 메서드는 숫자를 문자열로 변환하여 반환합니다.
- 진법을 나타내는 2 ~ 36 사이의 정수값을 인수로 전달할 수 있습니다.
- 기본값은 10진법으로 지정됩니다.

## Example
```javascript
console.log((123).toString());                              // 123
console.log((123).toString(2));                             // 1111011
console.log((123).toString(8));                             // 173
console.log((123).toString(16), typeof (123).toString(16)); // 7b string
```
