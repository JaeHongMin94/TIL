# 타입변환

타입변환에는 명시적 타입 변환과 암묵적 타입 변환이 있다. 명시적 타입 변환(타입 캐스팅)은 개발자에 의도가 보이는 행위입니다. 
암묵적 타입 변환(타입 강제 변환)은 개발자의 의도와는 상관없이 타입이 변경되는 것을 말합니다.

## 명시적 타입 변환(타입 캐스팅)

명시적 타입 변환은 개발자의 의도에 따라 변환되는 타입입니다.

### 문자열 타입 변환

```
console.log(String(1), typeof String(1));           // 1 string
console.log(String(true), typeof String(true));     // true string
console.log(NaN.toString(), typeof NaN.toString()); // NaN string
console.log(7 + '', typeof (7 + ''));               // 7 string
```

### 숫자 타입 변환

```
console.log(Number('77'), typeof Number('77'));               // 77 number
console.log(Number(true), typeof Number(true));               // 1 number
console.log(parseInt('0.123'), typeof parseInt('0.123'));     // 0 number
console.log(parseFloat('0.123'), typeof parseFloat('0.123')); // 0.123 number
console.log(+false, typeof +false);                           // 0 number
```

## 암묵적 타입 변환(타입 강제 변환)

암묵적 타입 변환은 발생하면 String, Number, Boolean과 같은 원시 타입 중 하나로 타입을 자동 변환한다.

### 문자열 타입 변환

```
console.log(77 + '', typeof (77 + ''));             // 77 string
console.log(true, typeof (true + ''));              // true string
console.log(null, typeof (null + ''));              // null string
console.log(Symbol() + '', typeof (Symbol() + '')); // TypeError: Cannot convert a Symbol value to a string
console.log({} + '', typeof ({} + ''));             // [object Object] string
```

- Symbol 타입은 String 타입으로 변환할수 없다.

### 숫자 타입 변환

```
console.log(+0, typeof +0);               // 0 number
console.log(3 * 10, typeof (3 * '10'));   // 30 number
console.log(0 + true, typeof (0 + true)); // 1 number
console.log(+[], typeof +{});             // 0 number
console.log(+{}, typeof +{});             // NaN number
```

- 빈 문자열(''), 빈 배열([]), false는 0으로, true는 1로 변환됩니다.
- 그 외에 타입들은 변환되지 않고 NaN이 됩니다.
