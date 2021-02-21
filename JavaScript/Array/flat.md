# Array.prototype.flat()

Array.prototype.flat() 메서드는 인수로 전달한 깊이만큼 재귀적으로 배열을 평탄화합니다.
```js
const arr = [1, [2, [3, [4]]]];

console.log(arr.flat());         // [ 1, 2, [ 3, [ 4 ] ] ]
console.log(arr.flat(2));        // [ 1, 2, 3, [ 4 ] ]
console.log(arr.flat().flat());  // [ 1, 2, 3, [ 4 ] ], 인수 2와 똑같이 출력된다.
console.log(arr.flat(Infinity)); // [ 1, 2, 3, 4 ], Infinity를 전달하게되면 배열 모두를 평탄화합니다.
```
