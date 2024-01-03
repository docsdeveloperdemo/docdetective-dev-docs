
  
   # **getUncoveredMatches**

## What does this do?

The `getUncoveredMatches` function takes a configuration object and a file object as input and returns an array of uncovered matches. Uncovered matches are markup elements that do not have a corresponding test.

## Why should I use this?

The `getUncoveredMatches` function can be used to identify areas of code that are not covered by tests. This information can be used to improve the test coverage of a codebase.

## Prerequisites

The `getUncoveredMatches` function requires the following prerequisites:

* A configuration object that specifies the markup elements to include in suggestions.
* A file object that contains the markup elements to be checked.

## How to use this

To use the `getUncoveredMatches` function, follow these steps:

1. Import the `getUncoveredMatches` function from the `doc-detective-core` module.
2. Create a configuration object that specifies the markup elements to include in suggestions.
3. Create a file object that contains the markup elements to be checked.
4. Call the `getUncoveredMatches` function with the configuration object and file object as arguments.
5. The function will return an array of uncovered matches.

## Example

The following example shows how to use the `getUncoveredMatches` function to identify uncovered matches in a codebase:

```javascript
const { getUncoveredMatches } = require('doc-detective-core');

const config = {
  suggestTests: {
    markup: ['TODO', 'FIXME'],
  },
};

const file = {
  file: 'path/to/file.js',
  markup: {
    TODO: [
      {
        line: 10,
        indexInFile: 20,
        text: 'TODO: Add a test for this function.',
      },
    ],
    FIXME: [
      {
        line: 20,
        indexInFile: 30,
        text: 'FIXME: This code is broken.',
      },
    ],
  },
};

const uncoveredMatches = getUncoveredMatches(config, file);

console.log(uncoveredMatches);
```

The output of the above example would be an array of two uncovered matches:

```json
[
  {
    line: 10,
    indexInFile: 20,
    text: 'TODO: Add a test for this function.',
    type: 'TODO',
    actions: ['addTest'],
  },
  {
    line: 20,
    indexInFile: 30,
    text: 'FIXME: This code is broken.',
    type: 'FIXME',
    actions: ['fixCode'],
  },
]
```
  
  