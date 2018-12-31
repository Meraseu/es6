# Advanced Use of Arrow Functions  

```
const double1 = number => 2 * number;
console.log(double1(8));
const double2 = (number1,number2) => (2 * number1) + (2 * number2);
console.log(double2(8,4));
const numbers = [1,2,3];
numbers.map(function(number) {
	return 2 * number;
});
numbers.map(number => 2 * number)
```