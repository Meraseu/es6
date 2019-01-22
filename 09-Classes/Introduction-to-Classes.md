# Introduction to Classes
```
function Car(options) {
  this.title = options.title;
}
Car.prototype.drive = function() {
  return 'vroom';
}
const car = new Car({ title: 'Focus'});
console.log(car) // Car {title: "Focus", constructor: Object}
console.log(car.drive()); // vroom
```