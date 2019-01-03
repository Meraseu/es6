# Enhanced Object Literals
```
function createBookShop(inventory) {
  return {
    inventory,
    inventoryValue() {
      return this.inventory.reduce((total, book) => {
        return total + book.price;
      }, 0);
    },
    priceForTitle(title) {
      return this.inventory.find(book => book.title === title);
    }
  };
}

const inventory = [
  {
    title: "Harry Potter",
    price: 10
  },
  {
    title: "Eloquent Javascript",
    price: 15
  }
];

const bookShop = createBookShop(inventory);

console.log(bookShop.inventoryValue()); // 25
console.log(bookShop.priceForTitle('Harry Potter')); // Object {title: "Harry Potter", price: 10}
```