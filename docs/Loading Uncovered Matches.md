
  
   # **getUncoveredMatches**

## What does this do?

The `getUncoveredMatches` function is used to load an array with uncovered matches. It iterates over the keys of the `file.markup` object and finds the markup configuration for each key. If the markup configuration is found, it checks if the markup is included in the `includeInSuggestions` array. If it is, it adds the uncovered matches for that markup to the `uncoveredMatches` array.

## Why should I use this?

The `getUncoveredMatches` function is useful for finding all of the uncovered matches in a file. This information can be used to generate suggestions for how to improve the documentation for the file.

## Prerequisites

Before using the `getUncoveredMatches` function, you must have the following:

* A configuration object that specifies the file types and markup types to be included in the suggestions.
* A file object that contains the markup for the file.

## How to use this

To use the `getUncoveredMatches` function, you must:

1. Create a configuration object that specifies the file types and markup types to be included in the suggestions.
2. Create a file object that contains the markup for the file.
3. Call the `getUncoveredMatches` function with the configuration object and the file object as arguments.
4. The function will return an array of uncovered matches.

## Example

The following example shows how to use the `getUncoveredMatches` function:

```
const config = {
  fileTypes: [
    {
      extensions: ['.js'],
      markup: [
        {
          name: 'markdown',
          actions: [
            {
              name: 'Add a code sample',
              description: 'Adds a code sample to the documentation.'
            },
            {
              name: 'Add a link to the documentation',
              description: 'Adds a link to the documentation for the method or class.'
            }
          ]
        }
      ]
    }
  ],
  suggestTests: {
    markup: ['markdown']
  }
};

const file = {
  file: '/Users/andrewvanbeek/dev-docs-work/clients/doc-detective-core/src/suggest.js',
  markup: {
    markdown: {
      uncoveredMatches: [
        {
          line: 10,
          indexInFile: 200,
          type: 'markdown',
          actions: [
            {
              name: 'Add a code sample',
              description: 'Adds a code sample to the documentation.'
            },
            {
              name: 'Add a link to the documentation',
              description: 'Adds a link to the documentation for the method or class.'
            }
          ]
        }
      ]
    }
  }
};

const uncoveredMatches = getUncoveredMatches(config, file);

console.log(uncoveredMatches);
```

The output of the above example will be an array of uncovered matches. Each match will contain the following information:

* The line number of the match.
* The index of the match in the file.
* The type of match.
* The actions that can be taken to address the match.
  
  