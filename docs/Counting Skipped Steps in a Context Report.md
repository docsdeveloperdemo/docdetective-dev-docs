
  
   # **contextReport.steps.filter((step) => step.result === "SKIPPED").length**

## What does this do?

The `contextReport.steps.filter((step) => step.result === "SKIPPED").length` method filters the `contextReport.steps` array for steps with a result of "SKIPPED" and returns the length of the resulting array.

## Why should I use this?

This method can be used to determine the number of steps in a context report that were skipped. This information can be useful for debugging purposes or for tracking the progress of a test run.

## Prerequisites

To use this method, you must have a context report object that contains an array of steps.

## How to use this

To use this method, simply call it on a context report object. The method will return the number of steps in the report that were skipped.

For example, the following code would log the number of skipped steps in a context report to the console:

```
const contextReport = {
  steps: [
    { result: "PASSED" },
    { result: "FAILED" },
    { result: "SKIPPED" },
    { result: "PASSED" },
  ],
};

const skippedSteps = contextReport.steps.filter((step) => step.result === "SKIPPED").length;

console.log(`There are ${skippedSteps} skipped steps in the context report.`);
```

## Output

The output of the above code would be:

```
There are 1 skipped steps in the context report.
```
  
  