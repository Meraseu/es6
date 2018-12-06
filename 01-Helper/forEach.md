# forEach
```
var colors = ['red','blue','green'];
colors.forEach(function(color) {
    console.log(color);
});
```
```
// Create an array of numbers
var numbers = [1,2,3,4,5];
// Create a variable to hold the sum
var sum = 0;
function adder(number) {
    sum += number;
}
// Loop over the array, incrementing the sum variable
numbers.forEach(adder);
// print the sum variable
console.log(sum);
```
```
var images = [
  { height: 10, width: 30 },
  { height: 20, width: 90 },
  { height: 54, width: 32 }
];
var areas = [];
[...images].forEach(element => {
  areas.push(element.height * element.width);
});
console.log(areas);
```