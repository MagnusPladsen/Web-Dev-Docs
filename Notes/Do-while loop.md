#js #javascript #webDev #dev #docs #js/loops

JavaScript provides several looping structures to perform repetitive tasks, and one of them is the do-while loop. The do-while loop is similar to the while loop in that it repeats a block of code while a condition is true, but with one key difference - it executes the block of code at least once, even if the condition is false.

## Syntax

The syntax for the do-while loop in JavaScript is as follows:

```
do {
  // code to be executed
} while (condition);

```

The code block will execute once before checking if the condition is true. If the condition is true, the block of code will execute again. This process will continue until the condition becomes false.

## Example

Let's take an example of a do-while loop that prints numbers from 1 to 5:

```
let i = 1;
do {
  console.log(i);
  i++;
} while (i <= 5);

```

In this example, the loop will first execute the code block and print 1 to the console. Then, it will check the condition `i <= 5`. Since `i` is now 2, which is less than or equal to 5, the loop will continue. The loop will execute the code block again, printing 2 to the console, and continue until it prints all numbers from 1 to 5.

## Use Cases

The do-while loop is useful when you want to execute a block of code at least once, regardless of whether the condition is met or not. It is commonly used in situations where you need to validate user input, as shown in the following example:

```
let num;
do {
  num = prompt("Please enter a number greater than 10");
} while(num <= 10);

alert("You entered " + num);

```

In this example, the user is prompted to enter a number greater than 10. If the user enters a number less than or equal to 10, the loop will execute again, prompting the user to enter a number until a valid input is provided.

## Conclusion

The do-while loop is a powerful looping structure in JavaScript that allows you to execute a block of code at least once, regardless of whether the condition is true or not. It can be used in various situations, including input validation and repetitive tasks that need to be executed at least once. Hopefully, this beginner's guide has helped you understand the basics of the do-while loop in JavaScript.



### [[Loops|<- Back to JavaScript/Loops]]