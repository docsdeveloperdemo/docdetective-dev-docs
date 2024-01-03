
  
   # **DocDetectiveCore.steps.filter((step) => step.result === "SKIPPED").length**

## What does this do?

The `DocDetectiveCore.steps.filter((step) => step.result === "SKIPPED").length` method returns the number of steps in the `DocDetectiveCore` that have been skipped.

## Why should I use this?

This method can be used to determine how many steps in the `DocDetectiveCore` have been skipped. This information can be useful for debugging purposes or for tracking the progress of a `DocDetectiveCore` run.

## Prerequisites

In order to use the `DocDetectiveCore.steps.filter((step) => step.result === "SKIPPED").length` method, you must first create a `DocDetectiveCore` object. You can do this by calling the `DocDetectiveCore()` constructor.

## How to use this

To use the `DocDetectiveCore.steps.filter((step) => step.result === "SKIPPED").length` method, simply call the method on a `DocDetectiveCore` object. The method will return the number of steps in the `DocDetectiveCore` that have been skipped.

Here is an example of how to use the `DocDetectiveCore.steps.filter((step) => step.result === "SKIPPED").length` method:

```
const docDetectiveCore = new DocDetectiveCore();

const skippedSteps = docDetectiveCore.steps.filter((step) => step.result === "SKIPPED").length;

console.log(`There are ${skippedSteps} skipped steps in the DocDetectiveCore.`);
```

## Output

The `DocDetectiveCore.steps.filter((step) => step.result === "SKIPPED").length` method will return a number. This number represents the number of steps in the `DocDetectiveCore` that have been skipped.
  
  