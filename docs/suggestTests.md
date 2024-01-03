
  
   # **suggestTests**

## What does this do?

The `suggestTests` function is used to generate test suggestions for a given configuration. It does this by first running code coverage on the configuration, and then using the coverage results to identify areas where tests are needed.

## Why should I use this?

The `suggestTests` function can be helpful for developers who are looking to improve the test coverage of their code. By identifying areas where tests are needed, developers can more easily write tests that will catch bugs and ensure that their code is working as expected.

## Prerequisites

In order to use the `suggestTests` function, you will need to have the following installed:

* Node.js
* The `doc-detective-core` package

## How to use this

To use the `suggestTests` function, simply import it into your code and call it with the desired configuration. The configuration object should contain the following properties:

* `source`: The path to the source code that you want to test.
* `tests`: The path to the directory where you want to save the test suggestions.
* `coverage`: The path to the coverage report that you want to use.

The `suggestTests` function will then generate test suggestions for the given configuration and save them to the specified directory.

## Example

The following example shows how to use the `suggestTests` function to generate test suggestions for a simple Node.js application:

```javascript
const suggestTests = require('doc-detective-core/suggestTests');

const config = {
  source: 'path/to/source/code.js',
  tests: 'path/to/test/directory',
  coverage: 'path/to/coverage/report.json'
};

suggestTests(config);
```

This will generate test suggestions for the `source/code.js` file and save them to the `test/directory` directory.
  
  