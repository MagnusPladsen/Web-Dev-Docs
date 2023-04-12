#js #javascript #webDev #dev #docs #js/scope

Scope is a concept where code is only accessible through a region or portion of code.

Scopes offer a number of advantages:

1.  Avoids namespace collisions: Variables with the same name but in different scopes can exist with there being a problem.
2.  Security: Variables inside of a scope cannot be accessed outside of that scope, protecting these variables from being accessed or altered.
3.  Saving memory: Variables inside of a block of code will stop existing once the block of code has finished running. For example, a variable created in an if statement will no longer exist once the if statement block of code has finished running.

### Global scope variables

A variable in global scope will be accessible throughout your app.

**NOTE:** You should avoid using global variables as much as possible. They can be changed anywhere in the app which can lead to errors and unpredictable results.

```
let value = 'Hello';

function displayValue() {
  console.log(value);
  // Logs:
  // Hello
}

displayValue();
```

A global variable can be changed anywhere in the app as it’s accessible anywhere in the app:

```
let value = 'Hello';

function displayValue() {
  value = 'World';
  console.log(value);
  // Logs:
  // World
}

displayValue();
```

### Local scope variables

Local scoped variables are only accessible in the block of code they are created in.

```
function displayValue() {
  let value = 'Hello';
}

// We are going to log 'value` which will throw an error because
//    it was created in the scope of the 'displayValue()' function
console.log(value);
// Logs:
// Uncaught ReferenceError: value is not defined
```

### Lexical scope

Lexical scope refers to the environment where a variable was defined, and how this variable can be accessed by nested functions. In other words, it refers to a function being able to access variables from the parent scope.

```
function outsideFunction() {
  const value = 'Hello world';

  function insideFunction() {
    // 'value' from the outside function can be accessed inside
    // of this nested function.
    console.log(value);
    // Logs:
    // 'Hello world'
  }

  insideFunction();
}

outsideFunction();
```

### Closure

A closure is the combination of a function and the lexical environment the function was declared in. The lexical environment contains any local variables that were in the scope at the time of creation.

```
function makeFunction(x) {
  return function (y) {
    return x + y;
  };
}

const add5 = makeFunction(5);

console.log(add5(2));
console.log(add5(5));

const add10 = makeFunction(10);
console.log(add10(20));
```

In the example above, `add5()` and `add10()` are closures. They have the same function logic, but also have their own lexical environments that have different values



### [[JavaScript|<- Back to JavaScript]]