# copyWithin()
> 범위 값 복사, 설정. 인덱스 범위의 값을 복사하여 같은 배열의 지정한 위치에 설정합니다.
```
const one = [1, 2, 3, 4, 5];
console.log(one.copyWithin(0,3)); // [4, 5, 3, 4, 5]
const two = [1, 2, 3, 4, 5];
console.log(two.copyWithin(0, 2, 4)); // [3, 4, 3, 4, 5]
const three = [1, 2, 3, 4, 5];
console.log(three.copyWithin(3)); // [1, 2, 3, 1, 2]
```
```
const arrayLike = { 0: "ABC", 1: "DEF", 2: "가나다", length: 3 };
const one = Array.prototype.copyWithin.call(arrayLike, 0, 1);
console.log(one); // Object {0: "DEF", 1: "가나다", 2: "가나다", length: 3}
function two() {
  return Array.prototype.copyWithin.call(arguments, 3, 0, 2);
}
console.log(two(1, 2, 3, 4, 5)); // [1, 2, 3, 1, 2]
```