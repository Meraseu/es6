# Prototypal Inheritance
```
function Car(options) {
  this.title = options.title;
}
Car.prototype.drive = function() {
  return 'vroom';
}
function Toyota(options) {
  Car.call(this, options);
  this.color = options.color;
}
Toyota.prototype = Object.create(Car.prototype);
Toyota.prototype.constructor = Toyota;
Toyota.prototype.honk = function() {
  return 'beep';
}
const toyota = new Toyota({ color:'red', title: 'Daily Driver'});
console.log(toyota); // Toyota {title: "Daily Driver", color: "red", constructor: Object}
console.log(toyota.drive()); // vroom
console.log(toyota.honk()); // beep 
```