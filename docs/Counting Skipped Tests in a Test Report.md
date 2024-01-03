
  
   # **specReport.tests.filter((test) => test.result === "SKIPPED").length**

## What does this do?

The `specReport.tests.filter((test) => test.result === "SKIPPED").length` method filters the `specReport.tests` array for tests with the result `"SKIPPED"` and returns the length of the filtered array.

## Why should I use this?

You can use this method to determine the number of skipped tests in a test report. This information can be useful for debugging and troubleshooting test failures.

## Prerequisites

To use this method, you must have a `specReport` object that contains a `tests` array. The `tests` array should contain objects that represent individual tests, each with a `result` property that indicates the status of the test.

## How to use this

To use this method, simply call it on the `specReport` object, passing in the filter function as an argument. The filter function should return `true` for tests that should be included in the filtered array, and `false` for tests that should be excluded.

For example, the following code snippet shows how to use the `specReport.tests.filter((test) => test.result === "SKIPPED").length` method to determine the number of skipped tests in a test report:

```javascript
const specReport = {
  tests: [
    {
      name: "Test 1",
      result: "PASSED"
    },
    {
      name: "Test 2",
      result: "SKIPPED"
    },
    {
      name: "Test 3",
      result: "FAILED"
    }
  ]
};

const skippedTests = specReport.tests.filter((test) => test.result === "SKIPPED").length;

console.log(`There are ${skippedTests} skipped tests in the test report.`);
```

The output of this code snippet would be:

```
There are 1 skipped tests in the test report.
```
  
  