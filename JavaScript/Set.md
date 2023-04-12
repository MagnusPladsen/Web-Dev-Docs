#js #javascript #webDev #dev #docs #js/set

A `Set` object stores unique values of any type. A value can only ever occur once in a `Set` and is therefore unique in a `Set`. You can also iterate through a `Set` in the order in which items were successfully added.

## Creating a new Set object[](https://content.noroff.dev/javascript-2/set.html#creating-a-new-set-object)

You create a new `Set` object with `new Set()`.

```
const mySet = new Set();
```

## Adding a value to a set[](https://content.noroff.dev/javascript-2/set.html#adding-a-value-to-a-set)

You can add a value to a set with the `add` method.

```
const mySet = new Set();

mySet.add('a');
// mySet is now ['a']
mySet.add('1');
// mySet is now ['a', 1]
```

## Check if a value exists[](https://content.noroff.dev/javascript-2/set.html#check-if-a-value-exists)

You can check if a value exists in a `Set` with the `has` method.

```
const mySet = new Set();

mySet.add('a');
// mySet is now ['a']

mySet.has('a');
// Returns true because 'a' is in the set

mySet.has('b');
// Returns false because 'b' is not in the set
```

## Delete an item from a set[](https://content.noroff.dev/javascript-2/set.html#delete-an-item-from-a-set)

You can delete an item from a set with the `delete` method.

```
const mySet = new Set();

mySet.add('a');
// mySet is now ['a']

mySet.delete('a');
// 'a' is now deleted from the set
```

## Getting the number of items in a set[](https://content.noroff.dev/javascript-2/set.html#getting-the-number-of-items-in-a-set)

You can get the number of items in a set with the `size` method.

```
mySet.add('a');
mySet.add('b');
// mySet is now ['a', 'b']

console.log(mySet.size);
// Logs:
// 2
```



### [[JavaScript|<- Back to JavaScript]]