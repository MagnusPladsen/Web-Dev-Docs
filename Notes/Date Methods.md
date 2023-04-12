#js #javascript #webDev #dev #docs #js/methods

The Date object is used to work with dates and times in JavaScript. It provides various methods to work with dates, which can be useful for calculating timelines, scheduling tasks, and handling user input. In this guide, we will explore some of the most commonly used Date methods in JavaScript.

## Getting the Current Date and Time

We can create a new Date object to get the current date and time using the `new Date()` constructor. For example:

```
const currentDate = new Date();
console.log(currentDate);

```

This will output the current date and time in your console, like this:

```
Thu Oct 21 2021 14:04:37 GMT-0400 (Eastern Daylight Time)

```

## Formatting Dates

To format a date in JavaScript, we can use the `toLocaleString()` method. This method takes an optional configuration object that allows us to specify which parts of the date we want to include. For example:

```
const options = { weekday: 'long', year: 'numeric', month: 'long', day: 'numeric' };
const formattedDate = currentDate.toLocaleString('en-US', options);
console.log(formattedDate);

```

This will output the current date in a more readable format, like this:

```
Thursday, October 21, 2021

```

## Getting Specific Date and Time Values

We can use various methods of the Date object to extract specific parts of the date and time. For example:

- `getFullYear()`: Returns the year (4 digits)
- `getMonth()`: Returns the month (0-11)
- `getDate()`: Returns the day of the month (1-31)
- `getDay()`: Returns the day of the week (0-6)
- `getHours()`: Returns the hour (0-23)
- `getMinutes()`: Returns the minute (0-59)
- `getSeconds()`: Returns the second (0-59)

Here is an example of how to use these methods:

```
const year = currentDate.getFullYear();
const month = currentDate.getMonth();
const day = currentDate.getDate();
const hour = currentDate.getHours();
const minutes = currentDate.getMinutes();
const seconds = currentDate.getSeconds();

console.log(`Today is ${day}/${month + 1}/${year}. The time is ${hour}:${minutes}:${seconds}.`);

```

This will output the current date and time in a customized format, like this:

```
Today is 21/10/2021. The time is 14:04:37.

```

## Summary

In this guide, we have covered some of the most commonly used Date methods in JavaScript. By using these methods, you can work with dates and times in your JavaScript applications, and perform various operations like formatting, extracting specific values, and more. With a little bit of practice, you can become proficient in working with dates and times in JavaScript.



### [[Methods|<- Back to JavaScript/Methods]]