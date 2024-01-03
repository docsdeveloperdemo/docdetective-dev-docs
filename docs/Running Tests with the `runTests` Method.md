
  
   # Running Tests with the `runTests` Method

## What does this do?

The `runTests` method in the `doc-detective-core` library iterates through a list of contexts and adds any supported contexts to an array.

## Why should I use this?

This method is useful for filtering out unsupported contexts from a list, allowing you to only run tests on the contexts that are supported by your application and platform.

## Prerequisites

Before using this method, you must:

- Install the `doc-detective-core` library.
- Import the `runTests` method into your code.

## How to use this

To use this method, you must provide the following parameters:

- `contexts`: An array of contexts to filter.
- `apps`: An array of apps to support.
- `platform`: The platform to support.

The method will return an array of supported contexts.

## Example

The following code sample shows you how to use the `runTests` method:

```javascript
const { runTests } = require('doc-detective-core');

const contexts = ['context1', 'context2', 'context3'];
const apps = ['app1', 'app2'];
const platform = 'platform1';

const supportedContexts = runTests(contexts, apps, platform);

console.log(supportedContexts);
```

## Output

The following output shows the supported contexts:

```
['context1', 'context2']
```
  
  