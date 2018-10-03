# JSON - JavaScript Object Notation
[Here](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object) is a resource and documentation on what is an object, please read and learn about what an object is, how it’s used, and what methods you can use on objects

## Creating Objects
Object [constructor](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object) 

```javascript
const person = new Object();
    person.firstname= “john”; 
    person.lastname = “appleseed”; 
    person.age = 50; 
    person.eyeColor = “blue”;
```
Object [initializer](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Object_initializer)

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
You can define or re-assign a property by assigning it a value using `=` as you would a normal variable

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


* WRONG: person.date of birth = '1994-06-17'; 
* RIGHT: person['date of birth] = '1994-06-17'; 


|dot-notation| bracket-notation|
|---|---|
|***Directly*** accesses a ***literally-named*** property of the object| ***Evaluates*** what's in the bracket ***before*** accessing the object|
| ***Cannot*** handle keys with spaces; property MUST be a valid JS identifier | ***Can*** handle keys with spaces (as a string)|
||Can be a ***variable***|

## Deleting Proterperties 
When deleting properties of an object, by extension, the value goes too. You need to use the [`delete`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/delete) operator:

```javascript
const classroom = {
    name: 'Cohort X', 
    count: 20, 
    city: 'Bronx', 
    transition: 'Oct 8th, 2018'
}; 

delete classroom.city; 

classroom
=> { name: 'Cohort X', count: 20, transtion: 'Oct 8th, 2018' }
```
## Object Methods

The value of an object can be anything in Javascript, meaning we can attach functions to 	object properties. When we do this, those functions becomes a method. 

There are also predetermined object methods that are preloaded on the browser that developers can use. Later on when you learn more about frameworks, and libraries, you can also use those predetermined methods

```javascript
// the following objects are exactly the same
let user = {
    sayHello: function(){
        alert("Hello"); 
    }
    firstname: "Kenny",
    lastname: "Cruzer",
}; 

let user = {
    sayHi() {
        alert("Hello"); 
    }
    name: "Kenny", 
    lastname: "Cruzer"
}
```

## This
*this* for objects references. 
In JS *this* is a keyword that refers to that current object *this* is used in. 

```javascript
// the following object are the exact same
const classCodeBridge = {
    name: 'cohort X', 
    count: 20, 
    transition: 'Oct 8th, 2018', 
    sayHeyCohortX(){
        console.log(`Hey this is ${this.name} and the class transitions to GA on ${this.transition}`)
    },
}

const classCodeBridge = {
    name: 'cohort X', 
    count: 20, 
    transition: 'Oct 8th, 2018', 
    sayHeyCohortX: function(){
        console.log('Hey this is ' + this.name + 'and the class transitions to GA on ' + this.transition)
    },
}

classCodeBridge.sayHeyCohortX()

=> Hey this is cohort X and the class transtions to GA on Oct 8th, 2018
```

## for ... in
[for...in](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for...in) statements iterates over all non-[Symbol](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Symbol), [enumerable properties](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Enumerability_and_ownership_of_properties) of an object 

```javascript
let phoneObject = {
    make: ‘Apple’,
    name: ‘iPhone XS’
    model: ‘A1920’,
    year: 2018, 
    color: ‘gold’,
}

let phoneFunction = () => {
    for(let i in phoneObject){
        console.log(`${phoneObject[i]}`)
    }
}
```

## Comparing Objects
In javascript if two objects are made seperately, they are completely different entities, even if their properties are identical. 

```javascript
const student = {name: 'Chris'};
=> undefined

const student2 = {name: 'Chris'};
=> undefined

student == student2
=> false

student === student
=> true
```