
  
   # **decideIntent**

## What does this do?

The `decideIntent` function is used to determine what action to take when a match is found in the code. It prompts the user to select an action from a list of options, and returns the selected action.

## Why should I use this?

The `decideIntent` function is useful for interactively deciding what to do with matches found in the code. It allows the user to choose the appropriate action to take, such as ignoring the match, replacing the match with a different string, or adding a comment to the code.

## Prerequisites

There are no prerequisites for using the `decideIntent` function.

## How to use this

To use the `decideIntent` function, pass in the match object and the filepath of the file where the match was found. The function will then prompt the user to select an action from a list of options. The selected action will be returned by the function.

Here is an example of how to use the `decideIntent` function:

```js
const match = {
  text: 'console.log("Hello, world!")',
  line: 10,
  type: 'console.log',
  actions: ['Ignore', 'Replace with `console.info`', 'Add comment']
};

const filepath = '/Users/andrewvanbeek/dev-docs-work/clients/doc-detective-core/src/suggest.js';

const action = decideIntent(match, filepath);

if (action) {
  // Take the appropriate action based on the selected action
}
```

## Relevant method or class

The `decideIntent` function is used in the `suggest` module to interactively decide what to do with matches found in the code. The `suggest` module is a command-line tool that helps developers write documentation for their code.
  
  