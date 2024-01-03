
  
   # **specReport.tests.filter((test) => test.result === "SKIPPED").length**

## What does this do?

The `specReport.tests.filter((test) => test.result === "SKIPPED").length` method filters the `specReport.tests` array to include only the tests that have a result of "SKIPPED". It then returns the length of the filtered array, which is the number of skipped tests.

## Why should I use this?

You can use this method to get the number of skipped tests in a test report. This can be useful for debugging purposes, or to track the progress of your testing efforts.

## Prerequisites

There are no prerequisites for using this method.

## How to use this

To use this method, simply call it on the `specReport` object. For example:

```
const skippedTests = specReport.tests.filter((test) => test.result === "SKIPPED").length;
```

This will assign the number of skipped tests to the `skippedTests` variable.

## Additional information

The `specReport.tests` array is a list of all the tests that were run in a test suite. Each test object has a `result` property that indicates the status of the test. The possible values for the `result` property are "PASSED", "FAILED", "SKIPPED", and "PENDING".
  
  