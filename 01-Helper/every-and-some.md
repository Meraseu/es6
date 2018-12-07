# every & some
```
const computers = [
  { name: "Apple", ram: 24 },
  { name: "Compaq", ram: 4 },
  { name: "Acer", ram: 32 }
];
let allComputersCanRunProgram = true;
let onlySomeCompotersCanRunProgram = false;

for (var i = 0; i < computers.length; i++) {
  var computer = computers[i];
  if (computer.ram < 16) {
    allComputersCanRunProgram = false;
  } else {
    onlySomeCompotersCanRunProgram = true;
  }
}

console.log(allComputersCanRunProgram);
console.log(onlySomeCompotersCanRunProgram);

allComputersCanRunProgram = computers.every(computer => {
  return computer.ram > 16;
});
onlySomeCompotersCanRunProgram = computers.some(computer => {
  return computer.ram > 16;
});
console.log(allComputersCanRunProgram);
console.log(onlySomeCompotersCanRunProgram);
```
```
const names = [
    'Alexandria',
    'Matthew',
    'Joe'
];
const isEvery = names.every(function(name) {
    return name.length > 4;
});
const isSome = names.some(function(name) {
    return name.length > 4;
});
console.log(isEvery); // And, result false
console.log(isSome); // Or, result true
```
```
function Field(value) {
  this.value = value;
}

Field.prototype.validate = function() {
  return this.value.length > 0;
};

const username = new Field("2cool");
const password = new Field("my_password");
const birthdate = new Field("10/10/2010");

const fields = [username, password, birthdate];

console.log(username.validate()); // true
console.log(username.validate() && password.validate()); // true

const formIsValid = fields.every(field => {
  return field.validate();
});
console.log(formIsValid); // true
```
```
var users = [
  { id: 21, hasSubmitted: true },
  { id: 62, hasSubmitted: false },
  { id: 4, hasSubmitted: true }
];
var hasSubmitted = users.every(({ hasSubmitted }) => hasSubmitted);
console.log(hasSubmitted); // false
```
```
const requests = [
  { url: "/photos", status: "complete" },
  { url: "/albums", status: "pending" },
  { url: "/users", status: "failed" }
];
const inProgress = requests.some(({ status }) => status === "pending");
console.log(inProgress);
```