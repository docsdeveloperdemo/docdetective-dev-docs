
  
   # **runCoverage**

## What does this do?

The `runCoverage` function is the entry point for the `doc-detective-core` library. It takes a configuration object as input and runs a series of checks to determine the test coverage and markup coverage of a set of files.

## Why should I use this?

The `runCoverage` function can be used to ensure that your code is well-tested and that your documentation is up-to-date. By running the `runCoverage` function, you can identify any areas where your code is not covered by tests or where your documentation is lacking.

## Prerequisites

Before using the `runCoverage` function, you must install the `doc-detective-core` library and configure it with your project settings.

## How to use this

To use the `runCoverage` function, simply call the function with a configuration object as input. The configuration object can be used to specify the files to be checked, the test coverage threshold, and the markup coverage threshold.

The `runCoverage` function will return a coverage report that contains information about the test coverage and markup coverage of the specified files.

## Example

The following example shows how to use the `runCoverage` function to check the test coverage and markup coverage of a set of files:

```javascript
const docDetectiveCore = require('doc-detective-core');

const config = {
  files: ['src/**/*.js'],
  testCoverageThreshold: 80,
  markupCoverageThreshold: 90
};

const coverageReport = docDetectiveCore.runCoverage(config);

console.log(coverageReport);
```

The output of the `runCoverage` function will be a coverage report that contains information about the test coverage and markup coverage of the specified files.
  
  