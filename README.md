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
You can define or re-assign a property by assigning it a value using = as you would a normal variable

```javascript
const person = {
    name: 'Ash'
}
person.name
=> 'Ash'

person.name = 'Gary'; 
person.name 
=> 'Gary'
```

## Braket vs Dot Notation
You can use bracket as well as dot notation, but it’s standard and better understood by other developers to use dot notation to access objects. 
```javascript
WRONG: person.date of birth = '1994-06-17'; 
RIGHT: person['date of birth] = '1994-06-17'; 
```

|dot-notation| bracket-notation|
|---|---|
|***Directly*** accesses a ***literally-named*** property of the object| ***Evaluates*** what's in the bracket ***before*** accessing the object|
| ***Cannot*** handle keys with spaces; property MUST be a valid JS identifier | ***Can*** handle keys with spaces (as a string)|
||Can be a ***variable***|