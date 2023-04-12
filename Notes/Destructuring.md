Destructuring allows us to make our code more concise and cleaner. We can destructure objects and arrays.

Destructuring lets us take properties from an object, or values from an array, without having to write multiple lines of code.

Try not to overthink destructuring, we are simply creating variables from objects/arrays in a concise manner.

## Destructuring Objects

To destructure an object we use the following syntax. In the curly braces `{ }` we add the properties we want to use from the object, and on the right, we add the object we want to destructure from:

```
const {
  /* properties here */
} = objectName;

// For example:
const { property1, property2 } = objectName;
```

### Dot notation

Let’s work through an example to demonstrate how to destructure:

Consider the following object which contains `firstName`, `lastName` and `country` properties:

```
const person = {
  firstName: 'Ola',
  lastName: 'Nordmann',
  country: 'Norway',
};

const greeting = `Hello, I am ${person.firstName} ${person.lastName} from ${person.country}.`;
console.log(greeting);
// Logs:
// Hello, I am Ola Nordmann from Norway.
```

In the above code, we have accessed the properties of `person` using dot notation. This ends up making our code quite long as we are writing out `person` multiple times.

### Assign properties to variables

Let’s assign the properties to variables this time to make the code more concise.

```
const person = {
  firstName: 'Ola',
  lastName: 'Nordmann',
  country: 'Norway',
};

const firstName = person.firstName;
const lastName = person.lastName;
const country = person.country;

const greeting = `Hello, I am ${firstName} ${lastName} from ${country}.`;
console.log(greeting);
// Logs:
// Hello, I am Ola Nordmann from Norway.
```

You can see that the code has become a lot shorter and it becomes easier to read.

There are 2 issues with this code when it comes to keeping our code clean:

1.  If we change our object name `person` to something else, such as `user`, we would have to change this in multiple places as we set variables to the parameters on multiple lines.
    
2.  If we had many properties and wanted to create variables from them, we would end up with many extra lines of code.
    

## Destructuring the properties
Let’s destructure the properties instead.

The syntax for destructuring is quite simple:

```
const {
  /* properties here */
} = objectName;

// For example:
const { property1, property2 } = objectName;
```

In the curly braces `{ }` we add the properties we want to destructure from the object. On the right of the `=` is the object we want to destructure from.

Let’s continue with our example from earlier. We will now destructure the `firstName`, `lastName` and `country` properties from the `person` object:

```
const person = {
  firstName: 'Ola',
  lastName: 'Nordmann',
  country: 'Norway',
};

// Destructured the properties here
const { firstName, lastName, country } = person;

const greeting = `Hello, I am ${firstName} ${lastName} from ${country}.`;
console.log(greeting);
// Logs:
// Hello, I am Ola Nordmann from Norway.
```

Let’s do a direct comparison of normal variable assignment to properties of the object vs destructuring:

```
const person = {
  firstName: 'Ola',
  lastName: 'Nordmann',
  country: 'Norway',
};

// Normal variable assignment to object properties
const firstName = person.firstName;
const lastName = person.lastName;
const country = person.country;

// Destructuring the values instead:
const { firstName, lastName, country } = person;
```

You can see above that our code is far more concise and maintainable.

## Destructuring parameters
You can destructure parameters which is a very common technique in JavaScript, Array methods and React.

Consider the following example:

```
function greetPerson(personObject) {
  const { firstName, lastName } = personObject;
  console.log(`Hello ${firstName} ${lastName}.`);
}

const person = {
  firstName: 'Ola',
  lastName: 'Nordmann',
};

greetPerson(person);
```

You could instead destructure the properties from the object where the parameter is:

```
function greetPerson({ firstName, lastName }) {
  console.log(`Hello ${firstName} ${lastName}.`);
}

const person = {
  firstName: 'Ola',
  lastName: 'Nordmann',
};

greetPerson(person);
```

Let’s have a look at the values being destructured in an Array method. You will see that we are using dot notation to assign the values to variables:

```
const people = [
  {
    firstName: 'Ola',
    lastName: 'Nordmann',
    score: 8,
  },
  {
    firstName: 'Kari',
    lastName: 'Nordmann',
    score: 9,
  },
  {
    firstName: 'Joakim',
    lastName: 'Nordmann',
    score: 4,
  },
];

const winners = people.filter((currentItem) => {
  if (currentItem.score >= 5) {
    return true;
  }
});
```

Let’s change the code so that it is destructured as a parameter:

```
const people = [
  {
    firstName: 'Ola',
    lastName: 'Nordmann',
    score: 8,
  },
  {
    firstName: 'Kari',
    lastName: 'Nordmann',
    score: 9,
  },
  {
    firstName: 'Joakim',
    lastName: 'Nordmann',
    score: 4,
  },
];

// Destructuring 'score' property from the current element
const winners = people.filter(({ score }) => {
  if (score >= 5) {
    return true;
  }
});
```

## Destructuring Arrays

Destructuring arrays is similar to destructuring objects, however, there are some differences. In objects, we have key/value pairs where we reference a value using a key. In arrays, we have a list of elements and use an index to reference an element. There aren’t keys in an array.

When we destructure from an array, we assign variable names to values from our array. The order in which we write our variable names directly relates to the order of the elements in the array.

```
const [
  /* values here */
] = arrayName;

// For example:
const [value1, value2] = arrayName;
```

### Array Destructuring Example 1

Let’s have a look at an array destructuring example. We have destructured the values at index 0 and index 1 to the values `x` and `y`:

```
const coords = [12, 30, 5, 9, 100, 53];

// 'x' is index 0 in the array
// 'y' is index 1 in the array
const [x, y] = coords;

console.log(x, y);
// Logs:
// 12 30
```

### Array Destructuring Example 2

Let’s have a look at another example. We have an array of names (`names`) and then destructure index 0 and index 1 to the variable names `name0` and `name1`.

```
const names = ['Ola', 'Kari', 'Joakim', 'Ole'];

// 'name0' is index 0 in the array
// 'name1' is index 1 in the array
const [name0, name1] = names;

console.log(name0, name1);
// Logs:
// Ola Kari
```

### Using the ‘rest’ parameter

If we destructure from an array, we can use the “rest parameter” to get the remainder of the array elements.

The syntax is simply `...rest`.

**NOTE:** You do not have to call the variable `rest`, you can use any name you would like.

```
const names = ['Ola', 'Kari', 'Joakim', 'Ole'];

// 'name0' is index 0 in the array
// 'name1' is index 1 in the array
const [name0, name1, ...rest] = names;

console.log(name0, name1);
// Logs:
// Ola Kari

console.log(rest);
// Logs:
// ['Joakim', 'Ole']
```

### Ignoring values
You can choose to ignore values by simply having no variable.

```
const values = [0, 1, 2, 3, 4];

const [value0, , value2] = values;
console.log(value0, value2);
// Logs:
// 0 2
```



### [[JavaScript|<- Back to JavaScript]]