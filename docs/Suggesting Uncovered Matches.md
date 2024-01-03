
  
   # **Suggest Uncovered Matches**

## What does this do?

The `suggestUncoveredMatches` function takes a file object and an array of markup types to include in suggestions. It then iterates over the markup types in the file, finds the markup configuration for each type, and adds any uncovered matches for that type to the array of uncovered matches.

## Why should I use this?

The `suggestUncoveredMatches` function can be used to find and suggest markup matches that have not yet been covered by the documentation. This can be helpful for improving the completeness of the documentation and ensuring that all markup is properly documented.

## Prerequisites

Before using the `suggestUncoveredMatches` function, you must have a file object that contains the markup to be checked and an array of markup types to include in suggestions.

## How to use this

To use the `suggestUncoveredMatches` function, simply call the function with the file object and the array of markup types as arguments. The function will then return an array of uncovered matches.

Here is an example of how to use the `suggestUncoveredMatches` function:

```js
const file = {
  markup: {
    bold: {
      uncoveredMatches: [
        {
          text: 'This is an uncovered match.',
          start: 0,
          end: 20,
        },
      ],
    },
    italic: {
      uncoveredMatches: [],
    },
  },
};

const includeInSuggestions = ['bold'];

const uncoveredMatches = suggestUncoveredMatches(file, includeInSuggestions);

console.log(uncoveredMatches);
```

The output of the above code would be an array of one uncovered match:

```js
[
  {
    text: 'This is an uncovered match.',
    start: 0,
    end: 20,
    type: 'bold',
    actions: ['bold'],
  },
]
```
  
  