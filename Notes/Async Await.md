#js #javascript #webDev #dev #docs #js/async

- `async...await` is syntactic sugar built on native JavaScript promises and generators.
- We declare an async function with the keyword `async`.
- Inside an `async` function we use the `await` operator to pause execution of our function until an asynchronous action completes and the awaited promise is no longer pending .
- `await` returns the resolved value of the awaited promise.
- We can write multiple `await` statements to produce code that reads like synchronous code.
- We use `try...catch` statements within our `async` functions for error handling.
- We should still take advantage of concurrency by writing `async` functions that allow asynchronous actions to happen in concurrently whenever possible.

Async/await is a powerful feature in JavaScript that allows us to write asynchronous code in a more synchronous style. It is built on top of promises and generators and simplifies the use of promises.

Here is an example of an async function that fetches data from an API:

```
async function fetchData() {
  try {
    const response = await fetch('<https://example.com/data>');
    const data = await response.json();
    console.log(data);
  } catch (error) {
    console.error(error);
  }
}

```

In this example, the `fetchData()` function is declared with the `async` keyword. Inside the function, we use the `await` keyword to pause execution until the promise returned by `fetch()` resolves. We then use another `await` keyword to pause execution until the promise returned by `response.json()` resolves. The resolved JSON data is then logged to the console.

Async/await is especially useful when we need to make multiple asynchronous requests in a specific order. Here is an example:

```
async function fetchMultipleData() {
  try {
    const response1 = await fetch('<https://example.com/data1>');
    const data1 = await response1.json();
    const response2 = await fetch('<https://example.com/data2>');
    const data2 = await response2.json();
    console.log(data1, data2);
  } catch (error) {
    console.error(error);
  }
}

```

In this example, we fetch two sets of data from two different endpoints, in sequence. Using async/await makes the code easier to read and understand compared to chaining promises.

It's important to note that async/await is not always the best choice. When we need to make multiple requests in parallel, it's better to use `Promise.all()` or other concurrency techniques.

Comparing to normal fetch, async/await simplifies the use of promises and avoids the need for chaining `then()` methods, making the code easier to read and understand. When using async/await, we can use `try...catch` statements for error handling, which is not possible with normal fetch.


### [[JavaScript|<- Back to JavaScript]]