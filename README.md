# TIL

## Table of Contents
- [About](#about)
- [Timeline](#timeline)

## About
A repository to record when (and what) I learned about new development-related languages, frameworks, tools, tips, or tricks.

## Timeline

### 2021-03-14

Today I learned that the ECMAScript spec once included a proposal for array comprehensions. I also learned that Firefox implemented this proposal, but that it has long since been removed: https://developer.mozilla.org/en-US/docs/Archive/Web/JavaScript/Array_comprehensions

For posterity: this proposal allowed JavaScript others to create new arrays from one or more 'source' arrays. The newly generated arrays may contain a subset of the original elements (eg. a filter operation has been applied), modified versions of the original elements (eg. a map operation has been performed), or both. See below for examples.

```
// Given an array containing the numbers 1 to 3, square them return the result.
[for (i of [1, 2, 3]) i * i] // Yields [1, 4, 9]

// Given an array containing the numbers 1 to 3, filter out odd numbers and return the result.
[for (i of [1, 2, 3]) if (i % 2 === 0) i] // Yields [2]

// Given an array containing the numbers 1 to 3, filter out odd numbers, square the remaining numbers, and return the result.
[for (i of [1, 2, 3]) if (i % 2 === 0) i * i] // Yields [4]

// Given two arrays, add the members who share the same index and return the result as a new array.
[for (i of [1, 2, 3]) for (j of [4, 5, 6]] i + j] // Yields [5, 7, 9]
```

### 2019-05-25

**Vim - :normal**

In Vim, the `:normal` and `:normal!` commands may be used to apply a series of keypresses to a selection of lines. For example, this command could be used to append a given character to a series of lines.

```
# Given a selection of lines, the following command will append the ';' character to each line.
:normal! A;
```

### 2018-06-10

**[Cypress](https://www.cypress.io/)**

A test-runner and accompanying UI for integration and end-to-end tests.

### 2018-05-27

**[`Error.captureStackTrace`](https://nodejs.org/api/errors.html#errors_error_capturestacktrace_targetobject_constructoropt)**

A method for storing the current state of the call stack in a given object. For example:

```
let myObj = {};

let myFn = () => {
    Error.captureStackTrace( myObj );
    console.log( myObj.stack ); // 'at MyFn'
}

myFn();
```

### 2018-05-24

**[Joi](https://github.com/hapijs/joi)**

A Node.js library for defining schema and validating object schema.

### 2018-05-23

**[React VR](https://facebook.github.io/react-360/)**

It exists!

### 2018-05-22

**[Fractal](https://fractal.build/)**

A tool for managing, displaying, and describing the markup and styles which make up a component library.

### 2018-05-21

**[Puppeteer](https://github.com/GoogleChrome/puppeteer)**

A node-based tool for running integration and end-to-end tests. Puppeteer can be used to test for the presence of elements on a page, to simulate user interaction, and to take capture the current view as a screenshot.

### 2018-05-14

**[jq](https://stedolan.github.io/jq/)**

A command line utility for parsing JSON data. `jq` can be used for displaying JSON data, extracting a given value, accessing nested data structures, and more.

### 2018-05-13

**[Sinon.JS](http://sinonjs.org/)**

Read up on [best practices for using `Sinon.JS`](https://semaphoreci.com/community/tutorials/best-practices-for-spies-stubs-and-mocks-in-sinon-js), including when and how to use the `spy`, `stub`, and `mock` methods.

### 2018-05-12

**[Sinon.JS](http://sinonjs.org/)**

Read all [documentation for `Sinon.JS@5`](http://sinonjs.org/releases/v5.0.7/).

### 2018-05-11

**[Sinon.JS](http://sinonjs.org/)**

A JavaScript library for mocking functions, faking asynchronous requests, and extracting data about functions called within unit tests. `Sinon.JS` ships with a mechanism for making assertions, although it may be used alongside other testing frameworks (eg. `Mocha`).
