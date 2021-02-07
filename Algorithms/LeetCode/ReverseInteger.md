# Reverse Integer

> https://leetcode.com/problems/reverse-integer/

- Given a signed 32-bit integer `x`, return `x` with its digits reversed. If reversing `x` causes the value to go outside the signed 32-bit integer range **[-2<sup>31</sup>, 2<sup>31</sup> - 1]**, then return `0`.<br>
부호있는 32비트 정수 x가 주어지면 숫자를 거꾸로 하여 x를 반환합니다. 반환한 수가 32비트 정수의 범위를 벗어나면 0을 반환합니다.

### Example 1 
- Input : x = 123
- Output : 321
  
### Example 2
- Input : x = -123
- Output : -321
  
### Example 3
- Input : x = 120
- Output : 21
  
### Example 4
- Input : x = 0
- Output : 0

## 처음에 주어진 코드
```javascript
var reverse = function(x) {
    
};
```

## 나의 풀이
- 정수를 받은 후 뒤집는다.
- 뒤집은 수가 32비트 범위를 벗어났다면(참) 0, 벗어나지 않았다면 값을 반환한다.
```javascript
function reverseInt(n) {
  const reversed = n.toString().split('').reverse().join('');
  if (Math.pow(-2, 31) >= parseInt(reversed) || Math.pow(2, 31) - 1 <= parseInt(reversed)) return 0;
  
  return parseInt(reversed) * Math.sign(n);
}
```

## 다른 사람의 풀이
- 정수를 받은 후 음수인지 양수인지 체크한다.
- 받은 정수를 거꾸로 돌려준다.
- 역으로 돌린 정수가 32비트 범위를 벗어나면 0을 반환하고, 벗어나지 않았다면 값을 반환한다.
```javascript
var reverse = function(x) {
    const isNegative = x < 0 ? -1 : 1
    const reverseN =  Number(Math.abs(x).toString().split('').reverse().join(''))
    if (reverseN > 0x7FFFFFFF) return 0
    return Number(Math.abs(x).toString().split('').reverse().join('')) * isNegative || 0
};
```
