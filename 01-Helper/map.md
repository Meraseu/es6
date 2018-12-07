# map
```
var numbers = [1, 2, 3];
var doubledNumbers = [];

for (var i = 0; i < numbers.length; i++) {
  doubledNumbers.push(numbers[i] * 2);
}
console.log(doubledNumbers);
// [2,4,6]
var doubled = numbers.map(function(number) {
  return number * 2;
});
console.log(doubled);
// [2,4,6]
```
```
const paints = [
  { color: "red" },
  { color: "blue" },
  { color: "yellow" },
  { fake: "dont_return" }
];
function pluck(array, property) {
  const filter = [];
  array.map(function(v) {
    v.hasOwnProperty(property) ? filter.push(v[property]) : "";
  });
  return filter;
}
const colors = pluck(paints, "color");
console.log(colors);
// ['red,'blue','yellow']
```