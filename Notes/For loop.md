#js #javascript #webDev #dev #docs #js/loops

A **for loop** is a type of loop that is commonly used in JavaScript. It is used to repeat a block of code a certain number of times, or until a specific condition is met. For loops are incredibly useful when you need to perform a repetitive task, such as iterating through an array or object.

## Syntax

The syntax for a for loop is as follows:

```
for (initialization; condition; increment/decrement) {
  // code to be executed
}

```

- `initialization`: This is where you set the starting value of the loop counter variable.
- `condition`: This is the condition that is checked before each iteration of the loop. If the condition is true, the loop will continue to run; if it is false, the loop will end.
- `increment/decrement`: This is where you change the value of the loop counter variable after each iteration of the loop.

## Example

Here is an example of a for loop that iterates through an array of numbers and prints each number to the console:

```
const numbers = [1, 2, 3, 4, 5];

for (let i = 0; i < numbers.length; i++) {
  console.log(numbers[i]);
}

```

In this example, the loop counter variable `i` is initialized to 0, and the loop will continue to run as long as `i` is less than the length of the `numbers` array. After each iteration of the loop, the value of `i` is incremented by 1.

## Use Cases

For loops are incredibly versatile, and can be used in a variety of different situations. Here are a few examples:

- Iterating through arrays or objects to perform a specific action on each item.
- Generating a sequence of numbers or letters.
- Performing a task a specific number of times.
- Checking for a specific condition within a set of data.

## Conclusion

For loops are an essential part of JavaScript programming, and are used in a wide range of applications. By understanding how to use for loops, you can make your code more efficient and effective, and perform complex operations with ease.



### [[Loops|<- Back to JavaScript/Loops]]