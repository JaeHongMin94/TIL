# TwoSum(두 수의 합)

> https://leetcode.com/problems/two-sum/

- Given an array of integers **nums** and an integer **target**, return indices of the two numbers such that they add up to **target**.<br>
정수의 배열(nums)과 정수 대상(target)이 주어지면 대상에 합산되도록 두 숫자의 인덱스를 반환합니다.
- You may assume that each input would have exactly one solution, and you may not use the same element twice.<br>
각 입력에는 정확히 하나의 해결책이 있다고 가정할 수 있으며, 동일한 요소를 두 번 사용할 수 없다.
- You can return the answer in any order.<br>
배열의 순서는 상관없음, 어떤 순서로든 결과값 반환 할 수 있습니다.

### Example 1 
- Input
  - nums = [2,7,11,15]
  - target = 9
- Output
  - [0,1]
  
### Example 2
- Input
  - nums = [3,2,4]
  - target = 6
- Output
  - [1,2]
  
### Example 3
- Input
  - nums = [3,3]
  - target = 6
- Output
  - [0,1]

## 처음에 주어진 코드
```JavaScript
var twoSum = function(nums, target) {
    
};
```

## 나의 풀이
- 순서대로 배열을 추출해서 값을 더해 sum에 넣어주고 target과 비교한다.
- 비교 후 참일 경우 두 수의 인덱스를 찾아 반환한다.
```javascript
const twoSum = function (nums, target) {
  var sum = 0;
  for (var i = 0; i < nums.length - 1; i++) {
    for (var j = 1; j < nums.length - 1; j++) {
      if (i === j) continue;
      sum = nums[i] + nums[j];
      if (sum === target) {
        var arr = [nums.indexOf(nums[i]), nums.lastIndexOf(nums[j])];
        return arr;
      }
    }
  }
};
 ```

## 다른 사람의 풀이
- 빈 배열을 생성하여 인덱스 값을 push() 메서드를 활용하여 값을 넣어 반환한다. 
```javascript
var twoSum = function (nums, target) {
    let length = nums.length
    let value
    let lastAns = []
    for (let i = 0; i <= length; i++) {
      for (let j = i + 1; j <= length; j++) {
        value = nums[i] + nums[j]
        if (value === target && i != j) {
          lastAns.push(i)
          lastAns.push(j)
          return lastAns
        }
      }
    }
  }
```

## 다른 사람의 풀이2
- map 객체를 활용하여 결과 값을 반환한다.
```javascript
var twoSum = function(nums, target) {
    let map = new Map();
    
    for(let i = 0; i<= nums.length - 1; i++){
        
        let current = nums[i];
        let opposite = target - current;
        
        if(map.has(opposite)){
            return [i, map.get(opposite)]
        }else{
            map.set(current,i)
        }
    }
  };
```
