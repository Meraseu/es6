# Tagged Template
```
const person = 'Mike';
const age = 28;
function myTag(strings, personExp, ageExp) {
  var str0 = strings[0]; // "that "
  var str1 = strings[1]; // " is a "
  var ageStr;
  if (ageExp > 99) {
    ageStr = 'centenarian';
  } else {
    ageStr = 'youngster';
  }
  return str0 + personExp + str1 + ageStr;
}
const result = myTag`that ${person} is a ${age}`;
console.log(result);
```