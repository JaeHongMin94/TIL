# Number.isSafeInteger() 

Number.isSafeInteger() 메서드는 인수로 전달된 값이 안전한 정수인지 검사합니다. 판별한 값은 Boolean값으로 반환합니다.
- 안전한 정수값은 **-(2<sup>53</sup> - 1) ~ 2<sup>53</sup> -1** 입니다.
- 전달된 값은 암묵적 타입 변화가 일어나지 않습니다.

## Example
```javascript 
console.log(Number.isSafeInteger(Math.pow(2, 53) - 1)); // true
console.log(Number.isSafeInteger(Math.pow(2, 53) + 1)); // false

console.log(Number.isSafeInteger(0.1));                 // false
console.log(Number.isSafeInteger(undefined));           // false
console.log(Number.isSafeInteger(Infinity));            // false
```
