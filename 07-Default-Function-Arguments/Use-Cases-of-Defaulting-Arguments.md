# Use Cases of Defaulting Arguments
```
function User(id) {
  this.id = id;
}
function generateId() {
  return Math.random() * 9999999;
}
function createAdminUser(user = new User(generateId())) {
  user.admin = true;
  return user;
}
const user = new User(generateId());
console.log(createAdminUser(user)); // User {id: 7103691.315701773, admin: true, constructor: Object}
```