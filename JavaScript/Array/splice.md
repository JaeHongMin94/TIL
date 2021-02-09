# Array.prototype.splice()

splice 메서드는 배열의 처음부터 끝가지 원하는 요소를 제거할 수 있습니다. **원본 배열을 직접 변경**합니다.

## splice 메서드의 3가지 매개변수

> splice(index, deleteCount, items)

- index : 제거할 요소의 배열 인덱스를 지정합니다.
- deleteCount : index부터 제거할 요소의 개수를 지정합니다.
  - 적지 않았을 경우에는 index부터 끝까지 제거합니다.
  - 0일 경우에는 제거되는 요소가 없습니다.
- items : 제거한 요소 위치에 삽입할 요소들의 목록입니다. 만약 삽입할 요소를 생략한다면 배열의 요소들만 제거합니다.

## 사용 예시
```javascript 
const arr = [1, 2, 3, 4, 5, 6, 7];
const result = arr.splice(3, 3, 8, 9, 10);

console.log(result); // [ 4, 5, 6 ]
console.log(arr);    // [ 1, 2, 3, 8, 9, 10, 7 ]
```
- splice(3, 3, 8, 9, 10)
  - index(3) : arr[3] 요소를 지정합니다.
  - deleteCount(3) : arr[3] 부터 3개의 요소를 제거합니다.
  - items(8, 9, 10) : 4, 5, 6 요소에 8, 9, 10 새로운 요소가 삽입됩니다.
- result에는 제거의 요소 [ 4, 5, 6 ]이 할당됩니다.
- arr은 요소를 제거하고 새롭게 들어간 요소를 합쳐 [ 1, 2, 3, 8, 9, 10, 7 ]으로 변경됩니다.

## deleteCount가 0일 경우
```javascript 
const arr = [1, 2, 3, 4, 5, 6, 7];
const result = arr.splice(3, 0);

console.log(result); // []
console.log(arr);    // [ 1, 2, 3, 4, 5, 6, 7]
```
- 아무런 요소도 제거되지 않고 result에 빈 배열 **[]** 이 할당됩니다.

## deleteCount가 0이지만 items에 요소가 있을 경우
```javascript 
const arr = [1, 2, 3, 4, 5, 6, 7];
const result = arr.splice(3, 0, 8, 9);

console.log(result); // []
console.log(arr);    // [ 1, 2, 3, 8, 9, 4, 5, 6, 7]
```
- 위와 같이 result에는 빈 배열 **[]** 이 할당 됩니다.
- 제거되는 요소는 없지만 arr[3] 위치부터 [ 8, 9 ] 요소들이 삽입됩니다.
