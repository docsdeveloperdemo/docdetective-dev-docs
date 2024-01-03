
  
   # **Uncovered Matches**

## What does this do?

The `uncoveredMatches` method in `doc-detective-core` takes a list of uncovered matches and adds them to the list of matches to be returned.

## Why should I use this?

This method is useful for adding matches that were not found by the initial search to the list of matches to be returned. This can be useful for adding matches that are found by a secondary search or for adding matches that are manually added by the user.

## Prerequisites

Before using the `uncoveredMatches` method, you must first create a list of uncovered matches. This can be done by using the `findUncoveredMatches` method in `doc-detective-core`.

## How to use this

To use the `uncoveredMatches` method, simply pass the list of uncovered matches to the method. The method will then add the matches to the list of matches to be returned.

Here is an example of how to use the `uncoveredMatches` method:

```
const uncoveredMatches = [
  {
    type: 'method',
    name: 'myMethod',
    args: ['arg1', 'arg2'],
    description: 'This method does something.'
  },
  {
    type: 'class',
    name: 'myClass',
    description: 'This class does something.'
  }
];

const matches = [];

uncoveredMatches.forEach((match) => {
  matches.push(match);
});

console.log(matches);
```

The output of the above code will be an array of matches that includes the uncovered matches.

## Conclusion

The `uncoveredMatches` method in `doc-detective-core` is a useful tool for adding matches that were not found by the initial search to the list of matches to be returned. This can be useful for adding matches that are found by a secondary search or for adding matches that are manually added by the user.
  
  