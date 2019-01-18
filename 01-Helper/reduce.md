# reduce
```
var numbers = [10, 20, 30];
var sum = 0;
for (var i = 0; i < numbers.length; i++) {
  sum += numbers[i];
}
console.log(sum); // result 60
const sum2 = numbers.reduce(function(sum, number) {
  return sum + number;
}, 50);
console.log(sum2);
```
```
var primaryColors = [
    {color : 'red'} ,
    {color : 'yellow'},
    {color : 'blue'}
];
var color = primaryColors.reduce(function(previous, primaryColor) {
    previous.push(primaryColor.color);
    return previous
}, []);
console.log(color);
```
```
function balancedParens(string) {
  return !string.split("").reduce((previous, char) => {
    if (previous < 0) {
      return previous;
    }
    if (char == "(") {
      return ++previous;
    }
    if (char == ")") {
      return --previous;
    }
  }, 0);
}
console.log(balancedParens(")("));
```
```
function sumMix(x) {
  return x.reduce((sum, value) => {
    return sum + (+value);
  }, 0);
}
sumMix([9, 3, '7', '3']); // 22
```