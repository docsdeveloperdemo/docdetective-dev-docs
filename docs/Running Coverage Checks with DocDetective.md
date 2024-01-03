
  
   # **runCoverage**

## What does this do?

The `runCoverage` function is the entry point for the `doc-detective-core` library. It takes a configuration object as input and runs a series of checks to determine the test coverage and markup coverage of a set of files.

## Why should I use this?

The `runCoverage` function can be used to identify areas of code that are not covered by tests or documentation. This information can be used to improve the quality of your codebase and ensure that it is well-tested and well-documented.

## Prerequisites

Before using the `runCoverage` function, you must install the `doc-detective-core` library and configure it with a configuration object. The configuration object can be used to specify the files to be checked, the test coverage threshold, and the markup coverage threshold.

## How to use this

To use the `runCoverage` function, simply call it with a configuration object as input. The function will return a coverage report that contains information about the test coverage and markup coverage of the specified files.

Here is an example of how to use the `runCoverage` function:

```javascript
const docDetective = require('doc-detective-core');

const config = {
  files: ['src/**/*.js'],
  testCoverageThreshold: 80,
  markupCoverageThreshold: 90
};

const coverageReport = docDetective.runCoverage(config);

console.log(coverageReport);
```

The output of the `runCoverage` function is a coverage report that contains the following information:

* **Test coverage:** The percentage of lines of code that are covered by tests.
* **Markup coverage:** The percentage of lines of code that are covered by documentation.
* **Files:** The list of files that were checked.
* **Test coverage details:** A list of the files that were checked, along with their test coverage percentages.
* **Markup coverage details:** A list of the files that were checked, along with their markup coverage percentages.

The coverage report can be used to identify areas of code that are not covered by tests or documentation. This information can be used to improve the quality of your codebase and ensure that it is well-tested and well-documented.
  
  