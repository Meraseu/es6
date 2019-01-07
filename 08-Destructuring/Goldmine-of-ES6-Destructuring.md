# Goldmine of ES6:Destructuring
```
var expense = {
  type: "Business",
  amount: "$45 USD"
};

var type = expense.type;
var amount = expense.amount;

// ES6

const { type, amount } = expense;

console.log(type); // Business
console.log(amount); // $45 USD
```