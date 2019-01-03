# Property value shorthand
```
function getCar(make, model, value) {
	return {
		make: make,
		model: model,
		value: value
	};
}
```
```
function getCar(make, model, value) {
	return {
		make,
		model,
		value
	};
}
```