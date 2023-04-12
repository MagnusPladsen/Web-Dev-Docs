#js #javascript #webDev #dev #docs #js/types/object 

In JavaScript, an object is a collection of properties. A property can be a value, a function, or another object. Objects are used to represent real-world entities, such as a person or a car, and to store data in a structured way.

## Creating an Object

There are two ways to create an object in JavaScript:

### 1. Object Literal

The easiest way to create an object is by using an object literal. An object literal is a comma-separated list of name-value pairs wrapped in curly braces {}.

Example:

```
let person = {
  name: "John",
  age: 30,
  city: "New York"
};

```

### 2. Constructor Function

Another way to create an object is by using a constructor function. A constructor function is a function that creates an object by setting properties and methods.

Example:

```
function Person(name, age, city) {
  this.name = name;
  this.age = age;
  this.city = city;
}

let person = new Person("John", 30, "New York");

```

## Accessing Object Properties

You can access object properties in two ways:

### 1. Dot notation

The dot notation is the most common way to access object properties.

Example:

```
console.log(person.name);

```

### 2. Bracket notation

The bracket notation is used when the property name contains special characters or spaces.

Example:

```
console.log(person["name"]);

```

## Converting an Object to a String

You can convert an object to a string by using the `JSON.stringify()` method.

Example:

```
let person = {name: "John", age: 30, city: "New York"};
let personString = JSON.stringify(person);
console.log(personString);

```

Output:

```
{"name":"John","age":30,"city":"New York"}

```

## Converting a String to an Object

You can convert a string to an object by using the `JSON.parse()` method.

Example:

```
let personString = '{"name":"John","age":30,"city":"New York"}';
let person = JSON.parse(personString);
console.log(person);

```

Output:

```
{name: "John", age: 30, city: "New York"}

```

## Use Cases

Objects are used in JavaScript for many purposes, such as:

- Storing data in a structured way
- Representing real-world entities
- Creating namespaces for functions and variables
- Passing data between functions and modules


### [[Types|<- Back to JavaScript/Types]]