#js #javascript #webDev #dev #docs #js/json #json

JSON stands for JavaScript Object Notation.

It is a way for us to store JavaScript data in a pure text format so that it can easily be shared, such as between applications or outside of a JavaScript environment.

## How it works
JSON is actually a very simple process and only contains two main aspects to it.

We convert our JavaScript data to JSON using `JSON.stringify()`. Then when we get JSON, we convert it to JavaScript data by using `JSON.parse()`.

## Convert to JSON (`JSON.stringify`)

We convert our JavaScript data to JSON so that it can easily be transferred. This is our JavaScript data that has been converted to pure text, like a string.

In this example, we convert a `person` object into JSON.

**NOTE:** Take note how the JSON we log has quotation marks around the keys whereas our JavaScript object doesn’t.

```
const person = {
  name: 'Ola Nordmann',
  id: 9,
  isAdmin: true,
};

const personJSON = JSON.stringify(person);

console.log(personJSON);
// Logs:
// {"name":"Ola Nordmann","id":9,"isAdmin":true}
```

## Converting JSON back to JavaScript (`JSON.parse`)

When we get JSON data we need to convert it to JavaScript so that we can start using it in our code. This is where we parse the JSON, which is pure text, into JavaScript code.

In this example we have JSON data which we convert into JavaScript code:

```
const personJSON = '{ "name": "Ola Nordmann", "id": 9, "isAdmin": true }';

const person = JSON.parse(personJSON);

console.log(person);
// Logs:
// {name: 'Ola Nordmann', id: 9, isAdmin: true}
```



### [[JavaScript|<- Back to JavaScript]]