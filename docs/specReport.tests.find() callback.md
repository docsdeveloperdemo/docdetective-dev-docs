
  
   # **DocDetective.findFailingTests**

## What does this do?

The `DocDetective.findFailingTests` method finds all the failing tests in a given spec report.

## Why should I use this?

This method can be used to quickly identify which tests are failing in a spec report, which can be helpful for debugging purposes.

## Prerequisites

In order to use this method, you must have a spec report that contains the results of your tests.

## How to use this

To use this method, simply call it with the spec report as the argument. The method will return an array of all the failing tests in the spec report.

Here is an example of how to use this method:

```
const specReport = {
  tests: [
    {
      name: "test1",
      result: "PASS"
    },
    {
      name: "test2",
      result: "FAIL"
    },
    {
      name: "test3",
      result: "PASS"
    }
  ]
};

const failingTests = DocDetective.findFailingTests(specReport);

console.log(failingTests);
// Output: [ { name: 'test2', result: 'FAIL' } ]
```

## Additional notes

* This method only finds failing tests in the spec report. It does not find tests that have been skipped or ignored.
* This method is not case-sensitive. It will find failing tests regardless of the case of the test names.
  
  