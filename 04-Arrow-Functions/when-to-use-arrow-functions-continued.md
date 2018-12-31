# When to Use Arrow Functions Continued  
```
const team = {
	members : ['Jane', 'Bill'],
	teamName : ['Super Squad'],
	teamSummary : function() {
		const self = this;
		return this.members.map(function(member) {
			return `${member} is on team ${self.teamName}`;
		});
	}
};
```
```
const team = {
	members : ['Jane', 'Bill'],
	teamName : ['Super Squad'],
	teamSummary : function() {
		return this.members.map((member) => `${member} is on team ${this.teamName}`);
	}
};
```