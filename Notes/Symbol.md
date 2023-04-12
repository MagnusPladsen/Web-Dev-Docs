#js #javascript #webDev #dev #docs #js/types/symbol 

Symbol is a primitive data type introduced in ES6 (ECMAScript 2015) that represents a unique identifier. A symbol value cannot be changed once it is created, and it is guaranteed to be unique. Symbol values are often used as property keys in objects, allowing for the creation of non-enumerable properties.

## Example

Here's an example of how to create a symbol in JavaScript:

```
const mySymbol = Symbol('description');
console.log(mySymbol); // Symbol(description)

```

In the above code, we create a new symbol using the `Symbol()` function and passing in a description as an optional parameter. The `console.log()` statement logs the created symbol to the console.

## Use Cases

1. Creating non-enumerable properties on an object

Symbols can be used to create non-enumerable properties on an object. This means that the property will not show up when iterating over the object using a `for...in` loop or the `Object.keys()` method.

```
const mySymbol = Symbol('description');
const myObj = {
  [mySymbol]: 'This is a non-enumerable property'
};

console.log(myObj[mySymbol]); // This is a non-enumerable property
console.log(Object.keys(myObj)); // []

```

In the above code, we create a new object with a property that uses the created symbol as its key. When we log the property value, we get the expected output. However, when we log the keys of the object using `Object.keys()`, we get an empty array because the symbol property is not enumerable.

1. Avoiding naming collisions

Symbols can also be used to create private members in a class or module, helping to avoid naming collisions. Because symbols are unique, there is no chance of two symbols having the same name.

```
const mySymbol = Symbol('description');
class MyClass {
  [mySymbol]() {
    console.log('This is a private method');
  }
}

const myInstance = new MyClass();
myInstance[mySymbol](); // This is a private method

```

In the above code, we create a new symbol and use it as a method name in a class definition. When we create an instance of the class and call the method using the symbol, we get the expected output.

## Conclusion

Symbols are a powerful addition to JavaScript that allow for the creation of unique identifiers and non-enumerable properties. They can be used in a variety of ways, including creating private members and avoiding naming collisions.



### [[Types|<- Back to JavaScript/Types]]