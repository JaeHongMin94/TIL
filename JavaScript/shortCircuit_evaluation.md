# 단축 평가(Short-Circuit Evaluation)

단축 평가는 코드는 논리 연산자를 유용하게 사용합니다.

```
true && true  // true
false && true // false
true || true  // true
false || true // true
```

단축 평가는 if문을 대체할 수 있습니다.

- && 평가
```javascript
if(true && true) console.log('참 입니다.')    // 참 입니다.
if(false && true) console.log('참 입니다.')   // 결과는 false이기 때문에 '참 입니다.' 문구가 나오지 않는다.

const isTrue = true && '참 입니다';
console.log(isTrue);                         // 참 입니다.

const isFalse = false && '참 입니다.';
console.log(isFalse);                        // false
```

- || 평가
```javascript
if(true || true) console.log('참 입니다.')    // 참 입니다.
if(false || true) console.log('참 입니다.')   // 참 입니다.

const isTrue = true || '참 입니다';
console.log(isTrue);                         // true

const isFalse = false || '참 입니다.';
console.log(isFalse);                        // 참 입니다.
```

- 삼항 연산자는 if...else문을 대체할 수 있습니다.
```javascript
if(true) console.log('참 입니다.');
else console.log('거짓 입니다.');             // 참입니다.

const isTrue = true ? '참 입니다.' : '거짓 입니다.';
console.log(isTrue);                         // 참 입니다.
```

