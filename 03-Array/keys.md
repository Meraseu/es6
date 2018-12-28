# keys()
> 배열의 각 인덱스를 키 값으로 가지는 새로운 Array Iterator 객체를 반환합니다.
```
const array = ['a', 'b', 'c'];
const iterator = array.keys();

for(let key of iterator) {
  console.log(key); // 0 1 2
}
```
```
const array = ['a',  , 'c'];
const sparseKeys = Object.keys(array);
const denseKeys = [...array.keys()];
console.log(sparseKeys); // ['0', '2']
console.log(denseKeys); // [0, 1, 2]
```