# More on When to Use Destructuring
```
const points = [[4, 5], [10, 1], [0, 40]];
const axios = points.map(([x, y]) => {
  return { x, y };
});
console.log(axios); // [Object, Object, Object]
```