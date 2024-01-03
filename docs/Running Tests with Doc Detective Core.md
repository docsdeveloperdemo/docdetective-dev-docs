
  
   # **runTests**

## What does this do?

The `runTests` function is the entry point for running tests using the Doc Detective Core library. It sets up the configuration, files, and test specs, and then runs the test specs and returns the results.

## Why should I use this?

The `runTests` function is a convenient way to run tests using the Doc Detective Core library. It handles all of the setup and configuration for you, so you can focus on writing your tests.

## Prerequisites

Before you can use the `runTests` function, you must have the following:

* A Doc Detective Core configuration file
* A set of test files
* A set of test specs

## How to use this

To use the `runTests` function, simply call it with the following arguments:

* `config`: The path to the Doc Detective Core configuration file
* `files`: The paths to the test files
* `specs`: The paths to the test specs

The `runTests` function will then run the tests and return the results.

## Example

The following example shows how to use the `runTests` function to run a set of tests:

```javascript
const runTests = require('doc-detective-core/src/index');

const config = 'path/to/config.json';
const files = ['path/to/file1.js', 'path/to/file2.js'];
const specs = ['path/to/spec1.js', 'path/to/spec2.js'];

runTests(config, files, specs).then((results) => {
  console.log(results);
});
```
  
  