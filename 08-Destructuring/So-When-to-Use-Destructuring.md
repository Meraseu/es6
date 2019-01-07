# So...When to Use Destructuring?
```
function signup({ username, password, email, dateOfBirth, city }) {
  // create new user
}

// other code
const user = {
  username: "myname",
  password: "mypassword",
  email: "myemail@example.com",
  dateOfBirth: "1/1/1990",
  city: "New York"
};
signup(user);
```