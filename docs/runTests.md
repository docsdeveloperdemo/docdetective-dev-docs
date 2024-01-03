
  
   # **runTests**

## What does this do?

The `runTests` function is the entry point for running tests using the Doc Detective Core library. It sets up the configuration, files, and test specifications, and then runs the test specifications.

## Why should I use this?

The `runTests` function is a convenient way to run tests using the Doc Detective Core library. It handles all of the setup and configuration for you, so you can focus on writing your tests.

## Prerequisites

Before you can use the `runTests` function, you must have the following prerequisites:

* Node.js installed
* The Doc Detective Core library installed

## How to use this

To use the `runTests` function, you must provide a configuration object. The configuration object can contain the following properties:

* `files`: An array of file paths to the files that you want to test.
* `specs`: An array of test specifications.
* `config`: An object containing any additional configuration options.

The `runTests` function will return an object containing the results of the tests. The results object will contain the following properties:

* `passed`: A boolean value indicating whether all of the tests passed.
* `failed`: An array of the tests that failed.
* `errors`: An array of any errors that occurred during testing.

## Example

The following example shows how to use the `runTests` function to run tests on a set of files:

```javascript
const { runTests } = require('doc-detective-core');

const config = {
  files: ['path/to/file1.js', 'path/to/file2.js'],
  specs: [
    {
      name: 'Test 1',
      description: 'This test checks that the function does what it is supposed to do.',
      test: () => {
        // Write your test here
      }
    }
  ]
};

runTests(config).then((results) => {
  if (results.passed) {
    console.log('All tests passed!');
  } else {
    console.log('Some tests failed:');
    console.log(results.failed);
  }
});
```
  
  