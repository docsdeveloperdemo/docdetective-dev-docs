
  
   # **parseTests**

## What does this do?

The `parseTests` function is responsible for parsing a set of test files and converting them into a structured format that can be used by the test runner. It supports both JSON and non-JSON test files, and can handle various types of test statements and markup.

## Why should I use this?

The `parseTests` function provides a convenient way to parse and validate test files, ensuring that they conform to the expected format and contain valid test steps. This helps to ensure the reliability and consistency of the test suite.

## Prerequisites

Before using the `parseTests` function, you should have a set of test files that you want to parse. These files can be in either JSON or non-JSON format, and should follow the specified file type extensions and test statement syntax.

## How to use this

To use the `parseTests` function, you can call it with the following parameters:

* `config`: A configuration object that specifies the file types and test statement syntax to be used.
* `files`: An array of file paths to the test files that you want to parse.

The function will return an array of parsed test specifications, each of which represents a single test file. These specifications can then be used by the test runner to execute the tests.

Here is an example of how you can use the `parseTests` function:

```javascript
const parseTests = require('./parse-tests');

const config = {
  fileTypes: [
    {
      extensions: ['.json'],
      testStartStatementOpen: '"tests": [',
      testStartStatementClose: ']',
      testEndStatement: '"id": ',
      stepStatementOpen: '"action": ',
      stepStatementClose: '}',
      markup: []
    },
    {
      extensions: ['.txt'],
      testStartStatementOpen: '// Test start',
      testStartStatementClose: '// Test end',
      testEndStatement: '// Test id: ',
      stepStatementOpen: '// Step action: ',
      stepStatementClose: '// Step end',
      markup: [
        {
          name: 'find',
          regex: /find (.*)/,
          actions: ['find']
        },
        {
          name: 'goTo',
          regex: /go to (.*)/,
          actions: ['goTo']
        }
      ]
    }
  ]
};

const files = ['test1.json', 'test2.txt'];

const specs = parseTests(config, files);

console.log(specs);
```

This example shows how to parse two test files, one in JSON format and the other in non-JSON format. The parsed test specifications are then logged to the console.
  
  