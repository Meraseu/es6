# The Rest on Rest and Spread
```
const defaultColors = ["red", "green"];
const userFavoriteColors = ["orange", "yellow"];
const fallColors = ["fire red", "fall orange"];
console.log([...fallColors, ...defaultColors, ...userFavoriteColors]); // ["fire red", "fall orange", "red", "green", "orange", "yellow"]

function validateShoppingList(...items) {
  if (items.indexOf("mile") < 0) {
    return ["milk", ...items];
  }
}
console.log(validateShoppingList("orange", "bread", "eggs")); // ["milk", "orange", "bread", "eggs"]
```