
  
   # **Suggest Uncovered Matches**

## What does this do?

The `suggestUncoveredMatches` function takes a file object and an array of markup types to include in suggestions. It then iterates over the markup types in the file, finds the markup configuration for each type, and adds any uncovered matches for that type to an array of uncovered matches.

## Why should I use this?

The `suggestUncoveredMatches` function can be used to find and suggest markup matches that are not currently covered by the documentation. This can be helpful for improving the accuracy and completeness of the documentation.

## Prerequisites

Before using the `suggestUncoveredMatches` function, you must have a file object and an array of markup types to include in suggestions.

## How to use this

To use the `suggestUncoveredMatches` function, simply pass the file object and the array of markup types to the function. The function will then return an array of uncovered matches.

Here is an example of how to use the `suggestUncoveredMatches` function:

```
const file = {
  markup: {
    bold: {
      uncoveredMatches: [
        {
          text: "This is an uncovered match.",
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

const markupTypes = ["bold", "italic"];

const uncoveredMatches = suggestUncoveredMatches(file, markupTypes);

console.log(uncoveredMatches);
```

The output of the above code would be:

```
[
  {
    text: "This is an uncovered match.",
    start: 0,
    end: 20,
    type: "bold",
    actions: ["bold"],
  },
]
```
  
  