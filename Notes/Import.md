#js #javascript #webDev #dev #docs #js/import 

Import statement is used to import functions, objects, or primitives which are exported from other modules. This allows us to use code from one module in another module.

## Import in Regular JavaScript

In regular JavaScript, the import statement is written as follows:

```
import { functionName } from './path/to/module.js';

```

Here, `functionName` is the name of the function which we want to import from the module. We can also use the `*` symbol to import all the exported functions from a module:

```
import * as module from './path/to/module.js';

```

## Import in ES6

In ES6, the import statement is written as follows:

```
import functionName from './path/to/module.js';

```

Here, we don't need to use curly braces for importing a single function. We can also use the `*` symbol to import all the exported functions from a module:

```
import * as module from './path/to/module.js';

```

## Default and Named Import

We can have both default and named exports in a module.

### Default Import

A default export is the one that is exported with the `default` keyword. We can import the default export using the following syntax:

```
import functionName from './path/to/module.js';

```

### Named Import

A named export is the one that is exported without the `default` keyword. We can import the named export using the following syntax:

```
import { functionName } from './path/to/module.js';

```

## Examples and Use Cases

Let's see an example of how to use the import statement in JavaScript.

Suppose we have a module named `math.js` which exports two functions: `add` and `subtract`.

```
// math.js
export function add(a, b) {
  return a + b;
}

export function subtract(a, b) {
  return a - b;
}

```

We can import these functions in another module as follows:

```
// app.js
import { add, subtract } from './math.js';

console.log(add(2, 3)); // Output: 5
console.log(subtract(5, 2)); // Output: 3

```

In the above example, we imported the `add` and `subtract` functions from `math.js` and used them in `app.js`.

We can also use the `*` symbol to import all the exported functions from a module:

```
// app.js
import * as math from './math.js';

console.log(math.add(2, 3)); // Output: 5
console.log(math.subtract(5, 2)); // Output: 3

```

In the above example, we imported all the exported functions from `math.js` using the `*` symbol and used them with the `math` object.

## Conclusion

The import statement is a powerful feature in JavaScript that helps us to use code from one module in another module. We can use the import statement in regular JavaScript as well as in ES6. We can have default and named exports in a module and can import them using the appropriate syntax.



### [[Import Export|<- Back to JavaScript/Import Export]]