# es6

## The 'forEach' Helper

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

## The 'map' Helper

```
var numbers = [1,2,3];
var doubledNumbers = [];

for(var i=0; i<numbers.length; i++) {   
    doubledNumbers.push(numbers[i] * 2);
}
console.log(doubledNumbers);
var doubled = numbers.map(function(number) {
    return number * 2;
});
console.log(doubled);
```
```
paints = [ { color: 'red' }, { color: 'blue' }, { color: 'yellow' }, { fake: 'dont_return' } ];
function pluck(array, property) {
    filter = [];
    array.map(function (v) {
        v.hasOwnProperty(property) ? filter.push(v[property]) : '';
    })
    return filter;
}
colors = pluck(paints, "color");
console.log(colors);
```

## The 'filter' Helper

```
var products = [
    {name : 'cucumber', type : 'vegetable'},
    {name : 'banana', type : 'fruit'},
    {name : 'celery', type : 'vegetable'},
    {name : 'orange', type : 'fruit'}
];
var filteredProducts = [];
for(var i=0; i<products.length; i++) {
    if(products[i].type === 'fruit') {
        filteredProducts.push(products[i]);
    }
}
console.log(filteredProducts);

filteredProducts = products.filter(function(product) {
    return product.type === 'vegetable';
});
console.log(filteredProducts);
```
```
var products = [
    {name : 'cucumber', type : 'vegetable', quantity : 0, price : 1},
    {name : 'banana', type : 'fruit', quantity : 10, price : 15},
    {name : 'celery', type : 'vegetable', quantity : 30, price : 15},
    {name : 'orange', type : 'fruit', quantity : 3, price : 5}
];
var filteredProducts = [];
filteredProducts = products.filter(function(product) {
    return product.type === 'vegetable' && product.quantity > 0 && product.price > 10
});
console.log(filteredProducts);
```
```
var post = {id : 4, title : 'New Post'};
var comments = [
    {postId : 4, content : 'awesome post'},
    {postId : 3, content : 'it was ok'},
    {postId : 4, content : 'neat'}
];
function commentsForPost(post, comments) {
    return comments.filter(function(comment) {
        return comment.postId === post.id
    });
}
console.log(commentsForPost(post, comments));
```

## The 'find' Helper

```
var users = [
    {name : 'Jill'},
    {name : 'Alex'},
    {name : 'Bill'}
];
var user;
for(var i=0; i<users.length; i++) {
    if(users[i].name === 'Alex') {
        user = users[i];
        break;
    }
}
console.log(user);

user = users.find(function(user) {
    return user.name === 'Alex';
});
console.log(user);
```

## The 'every' and 'some' Helper

```
var names = [
    'Alexandria',
    'Matthew',
    'Joe'
];
var isEvery = names.every(function(name) {
    return name.length > 4;
});
var isSome = names.some(function(name) {
    return name.length > 4;
});
console.log(isEvery); // And, result false
console.log(isSome); // Or, result true
```
```
function Field(value) {
    this.value = value;
}
Field.prototype.validate = function() {
    return this.value.length > 0;   
}
var username = new Field('2cool');
var password = new Field('my_password');
var birthdate = new Field('10/10/2010');

var formIsValid = [username, password, birthdate];

formIsValid.every(function(field) {
    return validate;
});
console.log(formIsValid);
```

## The 'reduce' Helper

```
var numbers = [10,20,30];
var sum = 0;
for(var i=0; i<numbers.length; i++) {
    sum += numbers[i];
}
console.log(sum); // result 60
numbers.reduce(function(sum, number) {
    return sum + number;
}, 0);
console.log(sum);
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

## Const/Let

```
// var name = 'Jane';
// var title = 'Soft Engineer';
// var hourlyWage = 40;

// ES6
const name = 'Jane';
let title = 'Soft Engineer';
let hourlyWage = 40;

// some time later...
title = 'Senior Soft Engineer';
hourlyWage = 45;
```
```
function count(targetString) {
	const characters = ['a','e','i','o','u'];
	let number = 0;
	
	for(var i=0; i<targetString.length; i++) {
		if(characters.includes(targetString[i])) {
			number++;
		}
	}
	return number;
}
console.log(count('aeiobxzceiaipbiox'));
```

## Template Strings

> Template Strings

```
function getMessage() {
	const year = new Date().getFullYear();
	return `The year is ${year}`;
}
console.log(getMessage());
```

> When to Reach for Template Strings  

```
const decivce_id = 4;
const guid = 20;
const username = 'hello';
const data = `{"device_id":"${decivce_id}", "guid":"${guid}", "username":"${username}"}`
console.log(data);

const year = 2016;
const yearMessage = `The year is ${year}`;
console.log(yearMessage);
```

## Arrow Functions

> Fat Arrow Functions  

'''
const add1 = function(a, b) {
	return a + b;
}
console.log(add1(1, 2));
// es6
const add2 = (a, b) => {
	return a + b;
}
add2(1, 2)
```

> Advanced Use of Arrow Functions  

'''
const double1 = number => 2 * number;
console.log(double1(8));
const double2 = (number1,number2) => (2 * number1) + (2 * number2);
console.log(double2(8,4));
const numbers = [1,2,3];
numbers.map(function(number) {
	return 2 * number;
});
numbers.map(number => 2 * number)
'''

> When to Use Arrow Functions  

'''
const team = {
	members : ['Jane', 'Bill'],
	teamName : ['Super Squad'],
	teamSummary : function() {
		const self = this;
		return this.members.map(function(member) {
			return `${member} is on team ${self.teamName}`;
		});
	}
};
console.log(team.teamSummary());
'''

> When to Use Arrow Functions Continued  

'''
const team = {
	members : ['Jane', 'Bill'],
	teamName : ['Super Squad'],
	teamSummary : function() {
		return this.members.map((member) => `${member} is on team ${this.teamName}`);
	}
};
console.log(team.teamSummary());
'''

## Enhanced Object Literals

## Default Function Arguments

## Rest and Spread Operator

## Destructuring

## Classes

## Generators

## Promises and Fetch