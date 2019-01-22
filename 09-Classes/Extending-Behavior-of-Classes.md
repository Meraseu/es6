# Extending Behavior of Classes
```
class Car {
  constructor({ title }) {
    this.title = title;
  }
  drive() {
    return "vroom";
  }
}
class Toyota extends Car {
  constructor(options) {
    super(options); // Car.constructor()
    this.color = options.color;
  }
  honk() {
    return "beep";
  }
}
const car = new Car({ title: "Toyota" });
console.log(car); // Car {title: "Toyota", constructor: Object}
console.log(car.drive()); // vroom

const toyota = new Toyota({ color: "red", title: "Daily Driver" });
console.log(toyota.honk()); // beep
console.log(toyota); // Toyota {title: "Daily Driver", color: "red", constructor: Object}
```