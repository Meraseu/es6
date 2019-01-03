# Computed property keys
```
function getCar(make, model, value) {
	var car = {};
	car['make' + make] = true;
	return car;
}
```
```
function getCar(make, model, value) {
	return {
		['make' + make]: true
	};
}
```