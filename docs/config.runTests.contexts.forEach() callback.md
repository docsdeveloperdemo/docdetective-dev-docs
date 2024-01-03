
  
   # **runTests**

## What does this do?

The `runTests` method runs the tests for the specified context.

## Why should I use this?

The `runTests` method is useful for testing the functionality of the SDK.

## Prerequisites

Before using the `runTests` method, you must:

1.  Install the `doc-detective-core` package.
2.  Create a test file that contains the tests that you want to run.
3.  Add the test file to the `tests` directory of your project.

## How to use this

To use the `runTests` method, you must:

1.  Import the `doc-detective-core` package.
2.  Create a `config.json` file that contains the configuration for the tests.
3.  Call the `runTests` method with the path to the `config.json` file as the first argument.

The following code sample shows you how to use the `runTests` method:

```javascript
const docDetectiveCore = require('doc-detective-core');

const config = {
  tests: [
    './tests/test1.js',
    './tests/test2.js',
  ],
  contexts: [
    'browser',
    'node',
  ],
  platforms: [
    'windows',
    'mac',
    'linux',
  ],
};

docDetectiveCore.runTests(config);
```

## Output

The `runTests` method will output the results of the tests to the console. The output will include the following information:

* The name of the test
* The status of the test (pass or fail)
* The error message (if the test failed)

## Troubleshooting

If you are having trouble using the `runTests` method, please refer to the following troubleshooting tips:

* Make sure that you have installed the `doc-detective-core` package correctly.
* Make sure that the `config.json` file is valid.
* Make sure that the test files are located in the `tests` directory of your project.
* Make sure that the tests are written correctly.

If you are still having trouble, please contact the doc-detective team for help.
  
  