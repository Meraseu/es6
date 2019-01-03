# Method definition shorthand
```
function getCar(make, model, value) {
	return {
		depreciate: function() {
			this.value -= 2500;
		}
	};
}
```
```
function getCar(make, model, value) {
	return {
		depreciate() {
			this.value -= 2500;
		}
	};
}
```