# fill()
> 같은 배열에서 인덱스 범위의 값을 지정한 값으로 바꾸어 반환합니다.
```
const one = [1, 2, 3];
console.log(one.fill(7)); // [7, 7, 7]

const two = [1, 2, 3, 4, 5];
console.log(two.fill(7, 1)); // [1, 7, 7, 7, 7]

const three = [1, 2, 3, 4, 5];
console.log(three.fill(7, 1, 3)); // 1, 7, 7, 4, 5]

const four = [].fill.call({ length: 3 }, 4);
console.log(four); // Object {0: 4, 1: 4, 2: 4, length: 3}

const five = Array(3).fill({});
five[0].hi = "hi";
console.log(five); // [{ hi: "hi" }, { hi: "hi" }, { hi: "hi" }]
```