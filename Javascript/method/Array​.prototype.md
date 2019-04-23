# Array.prototype  
Array 타임의 메소드들을 정리함  

## Array.prototype.findIndex  
주어진 판별 함수를 만족하는 첫번째 요소의 인덱스 값을 반환하는 함수  
```js  
const arr = [5, 6, 7, 8, 9];

function condition(element) {
  return element > 7;
}

console.log(arr.fintIndex(condition)); // output: 3
```  
