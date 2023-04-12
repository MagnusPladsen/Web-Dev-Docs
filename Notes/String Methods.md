#js #javascript #webDev #dev #docs #js/methods

JavaScript provides a variety of built-in functions and methods to manipulate strings. These functions can be used to perform various operations such as searching, replacing, concatenating, and converting strings.

Here are some commonly used String methods in JavaScript:

## 1. length()

The **length()** method returns the length of a string. It can be used to get the total number of characters in a string including spaces.

```
let str = "Hello World!";
console.log(str.length); // Output: 12

```

## 2. toUpperCase() and toLowerCase()

The **toUpperCase()** method converts all the characters in a string to uppercase, while the **toLowerCase()** method converts all the characters in a string to lowercase.

```
let str = "Hello World!";
console.log(str.toUpperCase()); // Output: HELLO WORLD!
console.log(str.toLowerCase()); // Output: hello world!

```

## 3. indexOf() and lastIndexOf()

The **indexOf()** method returns the index of the first occurrence of a specified substring in a string. If the substring is not found, it returns -1. The **lastIndexOf()** method works in a similar way, but returns the index of the last occurrence of the substring.

```
let str = "Hello World!";
console.log(str.indexOf("o")); // Output: 4
console.log(str.lastIndexOf("o")); // Output: 7

```

## 4. slice()

The **slice()** method extracts a portion of a string and returns it as a new string. It takes two arguments: the starting index and the ending index (optional). If the ending index is not provided, it extracts the rest of the string.

```
let str = "Hello World!";
console.log(str.slice(0, 5)); // Output: Hello
console.log(str.slice(6)); // Output: World!

```

## 5. replace()

The **replace()** method replaces a specified substring with another substring in a string. It takes two arguments: the substring to be replaced and the new substring.

```
let str = "Hello World!";
console.log(str.replace("World", "Universe")); // Output: Hello Universe!

```

These are just a few of the many String methods available in JavaScript. By using these methods, you can manipulate strings and perform various operations on them.



### [[Methods|<- Back to JavaScript/Methods]]