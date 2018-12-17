# Template Strings
```
function getMessage() {
	const year = new Date().getFullYear();
	return `The year is ${year}`;
}
console.log(getMessage());
```
```
const decivce_id = 4;
const guid = 20;
const username = 'hello';
const data = `{"device_id":"${decivce_id}", "guid":"${guid}", "username":"${username}"}`
console.log(data);

const year = 2016;
const yearMessage = `The year is ${year}`;
console.log(yearMessage);
```
