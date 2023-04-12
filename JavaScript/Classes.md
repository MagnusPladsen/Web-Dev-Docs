#js #javascript #webDev #dev #docs #js/classes

A class is a template for us to create objects, like a blueprint for the shape of the data.

In programming, a class contains properties and methods. Properties are variables inside of a class, and methods are functions inside of a class.

Classes form the basis for Object-Oriented Programming (OOP), a paradigm of programming.

Classes aren’t used very often in JavaScript, however, you will come across them at the workplace so it’s important to know how to use them.

## Basics

Consider the following class which contains a constructor, a method called `myMethod` and a property called `myInitialValue`:

```
class MyClass {
  // This is a property in our class
  basicProperty = 'My basic property';
  // This is another property however it isn't initialized to a value
  emptyProperty;
  // The constructor lets us set values when we create an instance of a class
  constructor(myInitialValue) {
    // A property 'myInitialValue' being initialized to an argument
    this.myInitialValue = myInitialValue;
  }

  // A method in the class
  myMethod() {
    console.log(this.myInitialValue);
  }
}

const myClassInstance = new MyClass('Hello world');
myClassInstance.myMethod();
// Logs:
// Hello world
```

### ‘new’ keyword

As mentioned, a class is a template of an object. We create a copy of a class, called an “instance”, which then has all of the properties and methods from the original class.

We create a new instance of a class by using the `new` keyword.

```
const myClassInstance = new MyClass('Hello world');
```

We can now call the `myMethod` method from this class:

```
// Logs "Hello world"
myClassInstance.myMethod();
```

### Constructor

The constructor in a class allows us to set any initial values that we’d like to set, such as a user’s name. These values can be passed in or be static.

In this example we set a value `myInitialValue` that’s being passed into the class:

```
constructor(myInitialValue) {
  this.myInitialValue = myInitialValue;
}
```

**NOTE:** You do not need to make use of a constructor if you have nothing to initialize.

### Methods

Methods are functions inside a class. They are copied when we create a new instance of a class.

We don’t use the `function` keyword when creating a method in a class, we simply write the method name:

```
class MyClass {
  // ... constructor

  // Method called 'myMethod'
  myMethod() {
    console.log(this.myInitialValue);
  }
}

// Create an instance of the class
const myClassInstance = new MyClass();
// Calling the 'myMethod' method
myClassInstance.myMethod();
```

### ‘this’ keyword

To access our variables inside of the class, we need to make use of the `this` keyword.

```
myMethod() {
  console.log(this.myInitialValue);
}
```

### Strict mode

The code in the body of a class is in “strict mode”.

## Practical example 1: Person object

Now that we’ve covered the basics, let’s start looking at a more practical example:

The following is a basic example of a class called `User`. It takes in `firstName` and `lastName` parameters and has a method `greetUser()` which logs a greeting message.

```
class User {
  language = 'Norwegian';
  constructor(firstName, lastName) {
    // Set 'firstName' to the 'firstName' parameter
    this.firstName = firstName;
    // Set 'lastName' to the 'lastName' parameter
    this.lastName = lastName;
  }

  // 'greetUser' method that logs a greeting message
  greetUser() {
    console.log(
      `Hello ${this.firstName} ${this.lastName}! Language: ${this.language}`,
    );
  }
}

const newUser = new User('Ola', 'Nordmann');
// Logs "Hello Ola Nordmann! Language: Norwegian"
newUser.greetUser();
```

## Practical example 2: Shopping Cart

We are going to have a look at a more complex implementation of a class.

In this example, we are going to create a Shopping Cart.

This class has:

-   `addToCart`: A function to add to the cart.
-   `removeFromCart`: Removes an item from the cart.
-   `calculateTotalCost`: Calculates the total cost of the items in the cart.
-   `displayCart`: Displays the items from the cart.
-   `displayTotalCost`: Displays the total cost of the items in the cart.

```
class ShoppingCart {
  cart = [];

  constructor(shopName, currency) {
    this.shopName = shopName;
    this.currency = currency;
  }

  /** Adds the item to the cart **/
  addToCart(item) {
    this.cart.push(item);
  }

  /** Removes the item from the cart **/
  removeFromCart(item) {
    const idToFind = item.id;
    // Find the index to remove
    const indexToRemove = this.cart.findIndex(
      (currentItem) => currentItem.id === idToFind,
    );
    // If the index is -1 then it means no item was found, so
    //    we return null to break out of the function
    if (indexToRemove === -1) {
      return null;
    }
    // Filter the items and remove the item that matches our index
    const newCart = this.cart.filter((item, index) => index !== indexToRemove);
    // Set the cart to cart without the item by spreading out the array
    this.cart = [...newCart];
  }

  /** Calculates the total cost of items in the cart **/
  calculateTotalCost() {
    const totalCost = this.cart.reduce((total, item) => {
      total += item.price;
      return total;
    }, 0);
    return totalCost;
  }

  /** Displays the items in the cart **/
  displayCart() {
    console.log('Your cart:');
    console.log('-------------------');
    this.cart.forEach((item) => {
      console.log(item.title);
    });
    console.log('===================');
  }

  /** Displays the total cost of the items in the cart **/
  displayTotalCost() {
    console.log('Total items: ', this.cart.length);
    console.log('The total of the cart is:', this.calculateTotalCost());
  }
}

const myCart = new ShoppingCart('Norway Bakery', 'USD');

const cookies = { id: 23, title: 'Chocolate Chip Cookies', price: 20.0 };
const cake = { id: 45, title: 'Vanilla Cake', price: 30.0 };

myCart.addToCart(cookies); // Add an item
myCart.addToCart(cookies); // Add an item
myCart.addToCart(cake); // Add an item
myCart.displayCart(); // Display the cart
myCart.removeFromCart(cookies); // Remove an item
myCart.displayCart(); // Display the cart
myCart.displayTotalCost(); // Display total cost of the cart
```



### [[JavaScript|<- Back to JavaScript]]