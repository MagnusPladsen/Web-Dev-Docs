The `Map` object holds key/value pairs like a normal object. The original insertion order into a `Map` object is remembered whereas a normal object’s order is unreliable. Any value, both objects and primitive values may be used as a key or a value.

## Basics

### Creating a map
We can create a map using `new Map()` e.g.

```
// This creates a new Map
const myMap = new Map();
```

### Adding a key/value pair

We use the `set` method on a `Map` object to add a new key/value pair.

This `set` method takes two parameters:

1.  The key you are setting
    
2.  The value you are setting
    

```
const myMap = new Map();

// The 'a' key will be set to 1
myMap.set('a', 1);
```

### Getting a value from a Map

We use the `get` method on a `Map` object to get the value of a key.

```
const myMap = new Map();

myMap.set('a', 1);

console.log(myMap.get('a'));
// Logs:
// 1
```

### Deleting values from a Map

You can delete values from a `Map` using the `delete` method on a `Map` object.

```
const myMap = new Map();

myMap.set('a', 1);

myMap.delete('a');
```

### Getting the number of items in a Map

You can get the number of items in a `Map` with the `size` method.

```
const myMap = new Map();

myMap.set('a', 1);
myMap.set('b', 2);

console.log(myMap.size);
// Logs:
// 2
```

## Differences between a Map and a normal Object

A `Map` is like an object in that they both make use of key/value pairs. There are however some differences.

### Key types

A `Map`’s keys can be any value which includes function, objects and primitives. Object keys on the other hand must be either a String or a Symbol.

### Key order

The keys in a `Map` are ordered in the order in which they are added. The order of keys of an Object cannot be relied upon and you shouldn’t ever rely on the order of keys in an Object.

### Converting to JSON

There isn’t a built-in way to convert from a `Map` to JSON and vice versa.

You can however build functions that deal with this. More information regarding this can be found in [this StackOverflow thread](https://stackoverflow.com/questions/29085197/how-do-you-json-stringify-an-es6-map).



### [[JavaScript|<- Back to JavaScript]]