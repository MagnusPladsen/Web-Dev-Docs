#js #javascript #webDev #dev #docs #js/methods

Arrays are a fundamental part of programming in JavaScript. They are used to store lists of data and can contain any data type, including numbers, strings, and even other arrays. Array methods are used to manipulate and work with arrays in JavaScript. In this document, we will discuss some of the most commonly used Array methods in JavaScript.

## 1. push()

The push() method adds one or more elements to the end of an array and returns the new length of the array.

```
let fruits = ['apple', 'banana', 'orange'];
fruits.push('mango');
console.log(fruits); // output: ['apple', 'banana', 'orange', 'mango']

```

## 2. pop()

The pop() method removes the last element from an array and returns that element.

```
let fruits = ['apple', 'banana', 'orange'];
fruits.pop();
console.log(fruits); // output: ['apple', 'banana']

```

## 3. shift()

The shift() method removes the first element from an array and returns that element.

```
let fruits = ['apple', 'banana', 'orange'];
fruits.shift();
console.log(fruits); // output: ['banana', 'orange']

```

## 4. unshift()

The unshift() method adds one or more elements to the beginning of an array and returns the new length of the array.

```
let fruits = ['apple', 'banana', 'orange'];
fruits.unshift('mango');
console.log(fruits); // output: ['mango', 'apple', 'banana', 'orange']

```

## 5. slice()

The slice() method returns a shallow copy of a portion of an array into a new array object selected from begin to end (end not included) where begin and end represent the index of items in that array.

```
let fruits = ['apple', 'banana', 'orange'];
let citrus = fruits.slice(1, 3);
console.log(citrus); // output: ['banana', 'orange']

```

## 6. splice()

The splice() method changes the contents of an array by removing existing elements and/or adding new elements.

```
let fruits = ['apple', 'banana', 'orange', 'mango'];
fruits.splice(2, 1, 'lemon', 'pear');
console.log(fruits); // output: ['apple', 'banana', 'lemon', 'pear', 'mango']

```

These are just a few of the many Array methods available in JavaScript. Understanding and mastering these methods will allow you to manipulate arrays and their contents with ease. Happy coding!



### [[Methods|<- Back to JavaScript/Methods]]