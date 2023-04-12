#js #javascript #webDev #dev #docs #js/export

Exporting is an essential concept in JavaScript that enables us to make functions, classes, and variables available to other modules.

## For Beginners

Exporting in JavaScript is accomplished using the `export` keyword. It allows us to make a function, variable, or class available to other modules. We can export a function or a variable in the following way:

```
// Exporting a variable
export const myVar = "Hello World";

// Exporting a function
export function myFunc() {
  console.log("Hello World");
}

```

In the above example, we are exporting a variable `myVar` and a function `myFunc`. Now, we can import these values in another module.

## Regular and ES6

In ES6, we have two ways of exporting: named and default.

### Named Exports

Named exports allow us to export multiple functions, classes, or variables from a single module. We can use the following syntax to export named values:

```
// Exporting multiple values
export const myVar1 = "Hello";
export const myVar2 = "World";

```

To import these values in another module, we can use the following syntax:

```
import { myVar1, myVar2 } from './myModule.js';

```

### Default Exports

Default exports allow us to export a single function, class, or variable from a module. We can use the following syntax to export default values:

```
// Exporting a single value
export default function myFunc() {
  console.log("Hello World");
}

```

To import this default value in another module, we can use the following syntax:

```
import myFunc from './myModule.js';

```

## Examples and Use Cases

Named exports are best suited for exporting multiple functions, classes, or variables from a single module. For example, in a utility module, we can export multiple utility functions like `sum`, `subtract`, `multiply`, and `divide` using named exports.

Default exports are best suited for exporting a single function, class, or variable from a module. For example, in a module that defines a class, we can export this class as a default export.

```
// Exporting a class as default
export default class MyClass {
  constructor() {
    //...
  }
}

```

In conclusion, exporting is an essential concept in JavaScript that enables us to make functions, classes, and variables available to other modules. We can use named exports to export multiple values and default exports to export a single value from a module.



### [[Import Export|<- Back to JavaScript/Import Export]]