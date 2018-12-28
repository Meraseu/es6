# entries()
> 배열의 각 인덱스에 대한 key/value 를 가지고 새로운 Array Iterator 객체를 반환합니다.
```
const values = [10, 20, 30];
const iterator = values.entries();
console.log(iterator.next()); // Object {value: Array[2], done: false}

for(var [key, value] of iterator) {
  console.log(key, ':', value); // 1 : 20, 2 : 30
}
```