# Object.prototype  
Object 타입의 메소드들을 정리함  

## Object.prototype.value  
전달된 객체가 가지는 값들로 이루어진 배열을 반환하는 메소드  
```js  
const obj1 = {a: '1', b: '2', c: '3'};
const obj2 = {a: 'hello', b: 3, c: 'world'}

console.log(Object.value(obj1)); // output: ['1', '2', '3']
console.log(Object.value(obj2)); // output: ['hello', 3, 'world']
```  

## Object.prototype.entries  
전달된 객체가 가지는 모든 값들에 대한 [key, value] 쌍을 요소로 가지는 배열을 반환하는 메소드  
```js  
const obj = {hey: 'hello', age: 25};
console.log(Object.entries(obj)); // [ ['hey', 'hello'], ['age', 25] ]
```  

## Object.prototype.keys  
전달된 객체가 가지는 요소들의 key 값을 요소로 가지는 배열을 반환하는 메소드  
```js  
const arr = ['hello', 'world', '!'];
const obj = {2: 'hellow', 7: 'world', 120: '!'};

console.log(Object.keys(arr)); // ['0', '1', '2']
console.log(Object.keys(obj)); // ['2', '7', '120']
```  
