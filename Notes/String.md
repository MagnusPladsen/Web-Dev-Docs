#js #javascript #webDev #dev #docs #js/types/string

In JavaScript, a string is a sequence of characters enclosed within single quotes (' ') or double quotes (" "). It can be used to represent text data, such as names, addresses, messages, etc. Here are some examples of string declaration in JavaScript:

```
let greeting = "Hello World!";
let name = 'John Doe';
let message = "It's a beautiful day!";

```

### Converting to String

Sometimes, you may need to convert a value to a string in JavaScript. This can be done using the `toString()` method or by concatenating the value with an empty string ('').

```
let num = 42;
let str1 = num.toString(); // "42"
let str2 = num + ''; // "42"

```

### String Methods

JavaScript provides several built-in methods for manipulating strings. Here are some commonly used methods:

- `length`: returns the length of the string
- `toUpperCase()`: converts the string to uppercase
- `toLowerCase()`: converts the string to lowercase
- `charAt(index)`: returns the character at the specified index
- `slice(start, end)`: extracts a portion of the string from the specified start to end index
- `indexOf(substring)`: returns the index of the first occurrence of a substring in the string
- `replace(oldValue, newValue)`: replaces all occurrences of the old value with the new value in the string

```
let str = "Hello World!";
console.log(str.length); // 12
console.log(str.toUpperCase()); // "HELLO WORLD!"
console.log(str.charAt(1)); // "e"
console.log(str.slice(0, 5)); // "Hello"
console.log(str.indexOf('o')); // 4
console.log(str.replace('o', 'x')); // "Hellx Wxrld!"

```

In conclusion, strings are an important data type in JavaScript and can be easily manipulated using various built-in methods.



### [[Types|<- Back to JavaScript/Types]]