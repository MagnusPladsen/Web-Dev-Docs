#js #javascript #webDev #dev #docs #js/spread

The spread syntax (`...`) allows you to “spread out” an array or object. This lets you very easily copy an array or object.

In this example, we create a new array from another array by spreading it out:

```
const oldArray = [0, 1, 2];

const newArray = [...oldArray];
console.log(newArray);
// Logs:
// [0, 1, 2]
```

Arrays and objects being passed by reference can be problematic. Spreading out arrays as a parameter is an easy way to solve this.

In this example, we use the spread syntax to create a new array which prevents us from mutating the initial array.

```
function changeValue(arrayIn) {
  const newArray = [...arrayIn];
  newArray.push('Hello world');
  console.log(newArray);
  // Logs:
  // [0, 1, 2, 'Hello world']
}

const initialArray = [0, 1, 2];
changeValue(initialArray);

console.log(initialArray);
// Logs:
// [0, 1, 2];
```

### Copying one array to another

The spread syntax allows us to very easily combine arrays.

In this example, we spread out two arrays to make a new array.

```
const array1 = [0, 1, 2];
const array2 = [3, 4, 5];

const newArray = [...array1, ...array2];
```

### Spreading objects

We can also spread objects.

In this example, we duplicate an object by spreading it out.

```
const myObject = {
  firstName: 'Ola',
  lastName: 'Nordmann',
};

const newObject = { ...myObject };
console.log(newObject);
// Logs
// {firstName: 'Ola', lastName: 'Nordmann'}
```



### [[JavaScript|<- Back to JavaScript]]