# Refactoring with Classes
```
class Car {
  constructor({ title }) {
    this.title = title;
  }
  drive() {
    return "vroom";
  }
}
const car = new Car({ title: "Toyota" });
console.log(car); // Car {title: "Toyota", constructor: Object}
console.log(car.drive()); // vroom
```