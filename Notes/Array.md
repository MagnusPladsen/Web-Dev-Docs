#js #javascript #webDev #dev #docs #js/types/array 

An array is a special variable, which can hold multiple values at the same time. In JavaScript, an array is a collection of data items that are of the same type. JavaScript arrays can hold different types of data such as strings, numbers, objects, and even other arrays.

## Creating an Array

In JavaScript, we can create an array using the following syntax:

```
let myArray = [item1, item2, item3, ...];

```

Here, `item1`, `item2`, and `item3` are the values or elements that we want to store in the array. We can also create an empty array and add elements later using the `push()` method.

```
let myArray = [];
myArray.push(item1);
myArray.push(item2);
myArray.push(item3);

```

## Accessing Array Elements

We can access the elements of an array using their index. In JavaScript, the index of the first element of an array is always 0. We can access an element of an array using the following syntax:

```
let myArray = [item1, item2, item3];
console.log(myArray[0]); // Output: item1
console.log(myArray[1]); // Output: item2
console.log(myArray[2]); // Output: item3

```

We can also change the value of an element by accessing it using its index and assigning a new value to it.

```
let myArray = [item1, item2, item3];
myArray[1] = "new value";
console.log(myArray); // Output: [item1, new value, item3]

```

## Array Methods

JavaScript provides several methods that we can use to manipulate arrays. Here are some of the most commonly used methods:

- `concat()` - joins two or more arrays and returns a new array.
- `push()` - adds one or more elements to the end of an array.
- `pop()` - removes the last element from an array.
- `shift()` - removes the first element from an array.
- `unshift()` - adds one or more elements to the beginning of an array.
- `slice()` - returns a new array containing a portion of the original array.
- `splice()` - adds or removes elements from an array.

## Examples

```
// Creating an array
let myArray = [1, 2, 3, 4, 5];

// Accessing array elements
console.log(myArray[0]); // Output: 1
console.log(myArray[1]); // Output: 2

// Changing array elements
myArray[1] = 10;
console.log(myArray); // Output: [1, 10, 3, 4, 5]

// Using array methods
myArray.push(6);
console.log(myArray); // Output: [1, 10, 3, 4, 5, 6]

let newArray = myArray.slice(1, 4);
console.log(newArray); // Output: [10, 3, 4]

// Iterating over an array
myArray.forEach(function(element) {
  console.log(element);
});

/* Output:
1
10
3
4
5
6
*/

// Use cases
Arrays are commonly used in JavaScript to store and manipulate data. They can be used to represent lists, queues, stacks, and more complex data structures. For example, we can use an array to store a list of items that a user has selected on a web page. We can also use an array to represent a collection of objects, such as the items in a shopping cart or the posts on a blog.

```



### [[Types|<- Back to JavaScript/Types]]