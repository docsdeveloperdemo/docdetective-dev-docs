
  
   # **testReport.contexts.filter((context) => context.result === "SKIPPED")**

## What does this do?

The `testReport.contexts.filter((context) => context.result === "SKIPPED")` method filters the `contexts` array of the `testReport` object to include only the contexts that have a `result` property with the value `"SKIPPED"`.

## Why should I use this?

This method can be used to easily identify and access the contexts that were skipped during a test run. This can be useful for debugging purposes or for generating reports on test coverage.

## Prerequisites

To use this method, you must have a `testReport` object that contains a `contexts` array. The `contexts` array must contain objects that have a `result` property.

## How to use this

To use this method, simply call it on the `testReport` object, passing in the `result` value that you want to filter by. For example, the following code would filter the `contexts` array to include only the contexts that were skipped:

```
const skippedContexts = testReport.contexts.filter((context) => context.result === "SKIPPED");
```

The `skippedContexts` variable would then contain an array of the contexts that were skipped.

## Example

The following example shows how to use the `testReport.contexts.filter((context) => context.result === "SKIPPED")` method to generate a report on the skipped tests:

```
const testReport = {
  contexts: [
    {
      name: "Context 1",
      result: "PASSED"
    },
    {
      name: "Context 2",
      result: "SKIPPED"
    },
    {
      name: "Context 3",
      result: "FAILED"
    }
  ]
};

const skippedContexts = testReport.contexts.filter((context) => context.result === "SKIPPED");

console.log("Skipped contexts:");
for (const context of skippedContexts) {
  console.log(`  ${context.name}`);
}
```

The output of this code would be:

```
Skipped contexts:
  Context 2
```
  
  