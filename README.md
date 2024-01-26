# -ES6-Syntax-Exercise-1-

Write a JavaScript program to compare two objects to determine if the first contains equivalent property values to the second one.

Use Object.keys() to get all the keys of the second object.
Use Array.prototype.every(), Object.prototype.hasOwnProperty() and strict comparison to determine if all keys exist in the first object and have the same values.

**Sample Solution:**

**JavaScript Code:**

//#Source https://bit.ly/2neWfJ2
const matches = (obj, source) =>
  Object.keys(source).every(key => obj.hasOwnProperty(key) && obj[key] === source[key]);
console.log(matches({ age: 25, hair: 'long', beard: true }, { hair: 'long', beard: true })); // true
console.log(matches({ hair: 'long', beard: true }, { age: 25, hair: 'long', beard: true })); // false
console.log(matches({ hair: 'long', beard: true }, { age: 26, hair: 'long', beard: true })); // false

**Sample Output:**

true
false
false
