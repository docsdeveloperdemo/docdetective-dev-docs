
  
   # **getSuggestions**

## What does this do?

The `getSuggestions` function generates a list of suggested tests based on the markup coverage of a set of files. It analyzes the uncovered matches in the markup and prompts the user to specify the intent of each match. Based on the user's input, it creates a test specification that includes a series of actions such as finding elements, capturing screenshots, navigating to URLs, checking links, making HTTP requests, and running shell commands.

## Why should I use this?

The `getSuggestions` function helps developers quickly and easily generate test cases for their code by leveraging the markup coverage of their documentation. This can save time and effort in the testing process and ensure that all aspects of the code are covered by tests.

## Prerequisites

To use the `getSuggestions` function, you will need the following:

- A set of files with markup coverage data.
- A configuration object that specifies the desired test generation settings.

## How to use this

To use the `getSuggestions` function, follow these steps:

1. Import the `getSuggestions` function from the `doc-detective-core` module.
2. Call the `getSuggestions` function with the configuration object and markup coverage data as arguments.
3. The function will return a test specification that includes a series of actions.
4. You can then use the test specification to generate test cases for your code.

## Example

The following example shows how to use the `getSuggestions` function to generate a test specification for a set of files:

```javascript
const { getSuggestions } = require('doc-detective-core');

const config = {
  // Configuration settings
};

const markupCoverage = {
  // Markup coverage data
};

const spec = getSuggestions(config, markupCoverage);

console.log(spec);
```

The output of the `getSuggestions` function will be a test specification that includes a series of actions. You can then use the test specification to generate test cases for your code.
  
  