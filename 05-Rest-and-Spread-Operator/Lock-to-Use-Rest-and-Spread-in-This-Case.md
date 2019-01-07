# Lock to Use Rest and Spread in This Case
```
const MathLibrary = {
  calculateProduce(...rest) {
    return this.multifly(...rest)
  },
  multifly(a, b) {
    return a * b;
  }
};
```