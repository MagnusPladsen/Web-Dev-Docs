#js #javascript #webDev #dev #docs #js/types/undefined 

In JavaScript, `undefined` is a primitive data type that indicates a variable has not been assigned a value. It is also used as the default return value of functions that do not explicitly return a value.

Here's an example of an undefined variable:

```
let myVar;
console.log(myVar); // Output: undefined

```

In this example, `myVar` is declared but not assigned a value, so its value is `undefined`.

Another way to get an undefined value is to access an object property that does not exist:

```
let myObj = {
  name: "John",
  age: 30
};

console.log(myObj.height); // Output: undefined

```

In this example, `myObj` has only two properties `name` and `age`. Accessing the `height` property returns `undefined` because it does not exist.

It's important to note that `undefined` is different from `null`, which is also a primitive data type in JavaScript. `null` is an explicitly assigned value that indicates the absence of any object value, while `undefined` indicates the absence of any value.

Here's an example of a function that returns `undefined`:

```
function returnUndefined() {
  // This function does not have a return statement
}

console.log(returnUndefined()); // Output: undefined

```

In this example, the `returnUndefined` function does not have a return statement, so it returns `undefined` by default.

## Conclusion

Understanding the concept of `undefined` in JavaScript is important for writing clean and error-free code. Always make sure to initialize your variables and handle cases where values may be undefined to avoid unexpected errors.



### [[Types|<- Back to JavaScript/Types]]