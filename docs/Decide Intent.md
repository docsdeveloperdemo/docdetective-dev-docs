
  
   # **decideIntent**

## What does this do?

The `decideIntent` function is used to determine what action to take when a match is found in the code. It prompts the user to select an action from a list of options, and returns the selected action.

## Why should I use this?

The `decideIntent` function is useful for interactively deciding what to do with matches found in the code. This can be helpful for quickly and easily making changes to the code without having to manually edit the documentation.

## Prerequisites

There are no prerequisites for using the `decideIntent` function.

## How to use this

To use the `decideIntent` function, simply call it with the match object and the filepath of the file where the match was found. The function will then prompt the user to select an action from a list of options, and return the selected action.

Here is an example of how to use the `decideIntent` function:

```js
const match = {
  type: 'method',
  text: 'myMethod()',
  line: 10,
  actions: ['ignore', 'document', 'delete']
};

const filepath = '/Users/andrewvanbeek/dev-docs-work/clients/doc-detective-core/src/suggest.js';

const action = decideIntent(match, filepath);

if (action) {
  // Do something with the selected action
}
```

## Additional notes

- The `decideIntent` function can be customized by providing a custom list of actions.
- The `decideIntent` function can be used in conjunction with other functions to automate the process of updating documentation.
  
  