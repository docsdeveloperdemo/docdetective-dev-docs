
  
   # **runCoverage**

## What does this do?

The `runCoverage` function is the entry point for the `doc-detective-core` library. It takes a configuration object as input and performs the following steps:

1. Sets the configuration object.
2. Sets the files to be analyzed.
3. Checks the test coverage for the files.
4. Checks the markup coverage for the files.
5. Returns the markup coverage.

## Why should I use this?

The `runCoverage` function can be used to generate documentation for your code. This documentation can help you understand how your code is used and how to use it effectively.

## Prerequisites

Before you can use the `runCoverage` function, you must install the `doc-detective-core` library. You can do this by running the following command:

```
npm install doc-detective-core
```

## How to use this

To use the `runCoverage` function, you must create a configuration object. The configuration object can contain the following properties:

* `files`: An array of files to be analyzed.
* `testCoverage`: A boolean value that indicates whether to check the test coverage for the files.
* `markupCoverage`: A boolean value that indicates whether to check the markup coverage for the files.

Once you have created the configuration object, you can call the `runCoverage` function and pass it the configuration object as an argument. The `runCoverage` function will then perform the steps described above and return the markup coverage.

## Example

The following example shows how to use the `runCoverage` function to generate documentation for a JavaScript file:

```javascript
const docDetectiveCore = require('doc-detective-core');

const config = {
  files: ['index.js'],
  testCoverage: true,
  markupCoverage: true
};

const markupCoverage = docDetectiveCore.runCoverage(config);

console.log(markupCoverage);
```

This example will generate documentation for the `index.js` file and print the markup coverage to the console.
  
  