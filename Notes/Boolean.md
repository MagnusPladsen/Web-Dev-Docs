#js #javascript #webDev #dev #docs #js/types/boolean 

Boolean is a data type in JavaScript that can have two values: `true` or `false`. It is used for logical operations, such as conditional statements and loops. In JavaScript, Boolean values are often used to test conditions and control program flow.

## Examples

Let's see some examples of how Boolean works in JavaScript:

### Example 1: Using Boolean in a conditional statement

```
let age = 18;
let canDrive = false;

if (age >= 16) {
  canDrive = true;
}

if (canDrive) {
  console.log("You can drive!");
} else {
  console.log("Sorry, you can't drive yet.");
}

```

In this example, we use the Boolean variable `canDrive` to determine if the person can drive based on their age. If the age is greater than or equal to 16, the value of `canDrive` is set to `true` and the person can drive.

### Example 2: Using Boolean in a loop

```
let i = 0;
let done = false;

while (!done) {
  console.log(i);
  i++;

  if (i === 5) {
    done = true;
  }
}

```

In this example, we use the Boolean variable `done` to control the loop. The loop continues until `done` is set to `true`. Inside the loop, we increment the value of `i` and print it to the console. When `i` reaches 5, we set `done` to `true`, and the loop ends.

## Conclusion

Boolean is an essential data type in JavaScript that is used for logical operations. It can have two values, `true` or `false`, and is often used to test conditions and control program flow. With the examples above, you should have a good understanding of how Boolean works in JavaScript.



### [[Types|<- Back to JavaScript/Types]]