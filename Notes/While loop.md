#js #javascript #webDev #dev #docs #js/loops

A loop is a programming construct that repeatedly executes a set of instructions until a specific condition is met. A `while` loop is a type of loop in JavaScript that executes a block of code as long as a specified condition evaluates to `true`. In this article, we will discuss what a while loop is, how it works, and provide some examples and use cases.

## Syntax

The syntax for a `while` loop is as follows:

```
while (condition) {
  // code block to be executed
}

```

The `condition` is a boolean expression that is evaluated before each iteration. If the condition evaluates to `true`, the code block is executed. Once the code block is executed, the condition is checked again, and if it is still `true`, the code block is executed again. This process continues until the condition evaluates to `false`.

## Example

```
let i = 0;
while (i < 5) {
  console.log(i);
  i++;
}

```

In this example, we declare a variable `i` and initialize it to `0`. The `while` loop continues to execute the code block as long as `i` is less than `5`. In each iteration, `i` is printed to the console, and `i` is incremented by `1`. The loop stops executing when `i` is equal to `5`.

## Use Cases

### 1. Repeating Actions until a Condition is Met

One of the most common use cases of a `while` loop is to repeat an action until a specific condition is met. For example, a programmer may want to prompt a user to enter their username and password until the correct combination is entered.

```
let username = "";
let password = "";
while (username !== "admin" || password !== "1234") {
  username = prompt("Enter your username:");
  password = prompt("Enter your password:");
}
alert("Welcome!");

```

In this example, the `while` loop continues to prompt the user for their username and password until the correct combination is entered. Once the correct combination is entered, the loop stops, and an alert is displayed.

### 2. Processing Arrays

Another use case for a `while` loop is to process arrays. In the following example, we use a `while` loop to iterate over an array of numbers and calculate their sum.

```
let numbers = [1, 2, 3, 4, 5];
let sum = 0;
let i = 0;
while (i < numbers.length) {
  sum += numbers[i];
  i++;
}
console.log(sum);

```

In this example, we declare an array of numbers and initialize the variable `sum` to `0`. We also declare a variable `i` and initialize it to `0`. The `while` loop continues to execute the code block as long as `i` is less than the length of the `numbers` array. In each iteration, the current element of the array is added to `sum`, and `i` is incremented by `1`. Once all elements of the array are processed, the loop stops, and the sum is printed to the console.

## Conclusion

In this article, we discussed what a `while` loop is, how it works, and provided some examples and use cases. While loops can be a powerful tool for repeating actions until a condition is met or processing arrays. However, they can also be dangerous if the condition is never met, leading to an infinite loop. Therefore, it is essential to ensure that the condition is updated correctly in each iteration to avoid such situations.



### [[Loops|<- Back to JavaScript/Loops]]