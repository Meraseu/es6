# Destructuring Arrays and Objects *At the Same Time*
```
const Google = {
  locations: ["Mountain View", "New York", "London"]
};
const {
  locations: [location]
} = Google;
console.log(location); // Mountain View 
```