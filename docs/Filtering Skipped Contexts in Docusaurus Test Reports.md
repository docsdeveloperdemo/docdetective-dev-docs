
  
   # **testReport.contexts.filter((context) => context.result === "SKIPPED")**

## What does this do?

The `testReport.contexts.filter((context) => context.result === "SKIPPED")` method filters the `contexts` array of the `testReport` object, returning a new array containing only the contexts that have a `result` property equal to `"SKIPPED"`.

## Why should I use this?

This method can be used to easily identify and access the contexts that were skipped during a test run. This can be useful for debugging purposes, or for generating reports on the results of a test run.

## Prerequisites

To use this method, you must first have a `testReport` object that contains a `contexts` array. This object can be obtained from the `getTestReport()` method of the `DocDetective` class.

## How to use this

To use this method, simply call it on the `testReport` object, passing in the `result` value that you want to filter by. For example, the following code would return an array of all the contexts that were skipped during a test run:

```
const skippedContexts = testReport.contexts.filter((context) => context.result === "SKIPPED");
```

## Example

The following example shows how to use the `testReport.contexts.filter((context) => context.result === "SKIPPED")` method to generate a report on the results of a test run:

```
const testReport = docDetective.getTestReport();

const skippedContexts = testReport.contexts.filter((context) => context.result === "SKIPPED");

console.log("The following contexts were skipped during the test run:");
for (const context of skippedContexts) {
  console.log(`  - ${context.name}`);
}
```

This example would output the following report:

```
The following contexts were skipped during the test run:
  - Context 1
  - Context 2
  - Context 3
```
  
  