# JSON - JavaScript Object Notation
[Here](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object) is a resource and documentation on what is an object, please read and learn about what an object is, how it’s used, and what methods you can use on objects

## Creating Objects
Object constructor 

```javascript
const person = new Object();
    person.firstname= “john”; 
    person.lastname = “appleseed”; 
    person.age = 50; 
    person.eyeColor = “blue”;
```
Object literal syntax

```javascript
const person = {
    name: 'john', 
    lastname: 'appleseed', 
    age: 50, 
    eyecolor: 'brown'
}
```
## Object Properties 
Objects in JS always have properties associated with them, in a Javascript object we can access values of an object using ‘dot notation’

```javascript
const person = {
    name: 'Ash', 
    last: 'Ketchum'
}
person.name
=> 'Ash'
```