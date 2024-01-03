
  
   # **Suggesting Uncovered Matches**

## What does this do?

This code suggests uncovered matches for a given file. It iterates through the markup keys of the file, finds the corresponding markup configuration, and adds any uncovered matches to the list of uncovered matches.

## Why should I use this?

This code is useful for finding and suggesting uncovered matches in a file, which can help to improve the accuracy and completeness of the documentation.

## Prerequisites

To use this code, you will need to have the following:

* A file with markup
* A file type configuration object
* A list of markup actions

## How to use this

To use this code, follow these steps:

1. Import the `suggest` function from the `doc-detective-core` library.
2. Call the `suggest` function with the following parameters:
    * `file`: The file with markup.
    * `fileType`: The file type configuration object.
    * `actions`: The list of markup actions.
3. The function will return a list of uncovered matches.

## Example

The following example shows how to use the `suggest` function to find and suggest uncovered matches for a file:

```javascript
const suggest = require('doc-detective-core/suggest');

const file = {
  markup: {
    bold: {
      uncoveredMatches: [
        {
          text: 'This is bold text.',
          start: 0,
          end: 15,
        },
      ],
    },
  },
};

const fileType = {
  markup: [
    {
      name: 'bold',
      actions: [
        {
          name: 'makeBold',
          description: 'Makes the selected text bold.',
        },
      ],
    },
  ],
};

const actions = [
  {
    name: 'makeBold',
    description: 'Makes the selected text bold.',
  },
];

const uncoveredMatches = suggest(file, fileType, actions);

console.log(uncoveredMatches);
```

The output of the above example will be a list of uncovered matches, which can then be used to improve the accuracy and completeness of the documentation.
  
  