#js #javascript #webDev #dev #docs #js/methods

Regular expressions (regex) are patterns used to match character combinations in strings. They are an important part of almost every programming language, including JavaScript. In this document, we will explore some of the most commonly used regex methods in JavaScript.

## RegExp()

The `RegExp()` constructor function is used to create a regular expression object. It takes two arguments: the pattern to match and an optional flag to specify the matching behavior. For example:

```
let regex = new RegExp('hello', 'i');

```

This creates a regular expression that matches the string 'hello' case-insensitively.

## test()

The `test()` method is used to test a string for a match with a regular expression. It returns `true` if there is a match and `false` otherwise. For example:

```
let regex = /hello/;
let result = regex.test('hello world');
console.log(result); // true

```

This code creates a regular expression that matches the string 'hello' and tests it against the string 'hello world'. Since there is a match, the `test()` method returns `true`.

## exec()

The `exec()` method is used to search for a match in a string with a regular expression. It returns an array containing information about the match, or `null` if there is no match. For example:

```
let regex = /hello (\\w+)/;
let result = regex.exec('hello world');
console.log(result); // ["hello world", "world"]

```

This code creates a regular expression that matches the string 'hello' followed by one or more word characters. It then searches the string 'hello world' for a match and returns an array with two elements: the entire match ("hello world") and the captured group ("world").

## match()

The `match()` method is used to search a string for a match with a regular expression. It returns an array containing the matches, or `null` if there is no match. For example:

```
let regex = /hello (\\w+)/;
let result = 'hello world'.match(regex);
console.log(result); // ["hello world", "world"]

```

This code creates the same regular expression as the previous example and uses the `match()` method to search for a match in the string 'hello world'. The resulting array is the same as before.

## replace()

The `replace()` method is used to replace a portion of a string with a new string. It takes two arguments: the regular expression to match and the replacement string. For example:

```
let regex = /hello (\\w+)/;
let result = 'hello world'.replace(regex, 'hi $1');
console.log(result); // "hi world"

```

This code creates the same regular expression as before and uses the `replace()` method to replace the entire match with the string "hi " followed by the captured group ("world").

## Conclusion

Regular expression methods are powerful tools for working with strings in JavaScript. By using these methods, you can easily search for and manipulate specific character combinations within a string. With practice, you can become proficient in using regular expressions for a wide variety of use cases.



### [[Methods|<- Back to JavaScript/Methods]]