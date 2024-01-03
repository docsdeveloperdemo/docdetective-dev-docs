
  
   # **getUncoveredMatches**

## What does this do?

The `getUncoveredMatches` function is used to load an array with uncovered matches. It iterates over the keys of the `file.markup` object and finds the corresponding `markConfig` object. If the `mark` is included in the `includeInSuggestions` array, it adds the uncovered matches for that mark to the `uncoveredMatches` array.

## Why should I use this?

The `getUncoveredMatches` function is useful for finding all of the uncovered matches in a file. This information can be used to generate suggestions for how to improve the documentation for the file.

## Prerequisites

Before using the `getUncoveredMatches` function, you must first:

1.  Load the `file` object.
2.  Load the `config` object.

## How to use this

To use the `getUncoveredMatches` function, simply call it with the following arguments:

```
getUncoveredMatches(config, file)
```

The function will return an array of uncovered matches.

## Example

The following code shows how to use the `getUncoveredMatches` function:

```
const config = {
  suggestTests: {
    markup: ['TODO', 'FIXME'],
  },
  fileTypes: [
    {
      extensions: ['.js'],
      markup: [
        {
          name: 'TODO',
          actions: ['Add test'],
        },
        {
          name: 'FIXME',
          actions: ['Fix bug'],
        },
      ],
    },
  ],
};

const file = {
  file: '/Users/andrewvanbeek/dev-docs-work/clients/doc-detective-core/src/suggest.js',
  markup: {
    TODO: [
      {
        line: 10,
        indexInFile: 20,
        text: 'Add test for this function.',
      },
    ],
    FIXME: [
      {
        line: 20,
        indexInFile: 40,
        text: 'Fix this bug.',
      },
    ],
  },
};

const uncoveredMatches = getUncoveredMatches(config, file);

console.log(uncoveredMatches);
```

The output of the above code will be:

```
[
  {
    line: 10,
    indexInFile: 20,
    text: 'Add test for this function.',
    type: 'TODO',
    actions: ['Add test'],
  },
  {
    line: 20,
    indexInFile: 40,
    text: 'Fix this bug.',
    type: 'FIXME',
    actions: ['Fix bug'],
  },
]
```
  
  