# values()
> 배열의 각 인덱스에 대한 값을 가지는 새로운 Array Iterator 객체를 반환합니다.
```
const array = ['a', 'b', 'c'];
const iterator = array.values();

for(let value of iterator) {
  console.log(value); // a b c
}
```
```
const array = ['w','y', 'k', 'o', 'p'];
const iterator = array.values();
for(const letter of iterator) {
  console.log(letter); // w y k o p
}
```
```
const array = ['w', 'y', 'k', 'o', 'p'];
const iterator = array.values();
console.log(iterator.next().value); // w
console.log(iterator.next().value); // y
console.log(iterator.next().value); // k
console.log(iterator.next().value); // o
console.log(iterator.next().value); // p
```