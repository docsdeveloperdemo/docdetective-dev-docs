
  
   # **checkMarkupCoverage**

## What does this do?

The `checkMarkupCoverage` function analyzes the coverage of markup (such as Markdown, HTML, or XML) in a set of files. It takes two parameters:

- `config`: A configuration object that specifies the markup types to be analyzed and the file types to be included.
- `testCoverage`: A test coverage object that contains information about which lines of code are covered by tests.

The function returns a `markupCoverage` object that contains the following information:

- `summary`: A summary of the markup coverage, including the total number of covered and uncovered lines of markup.
- `files`: An array of objects, each of which contains information about the markup coverage of a single file.
- `errors`: An array of errors that occurred during the analysis.

## Why should I use this?

The `checkMarkupCoverage` function can be used to identify areas of markup that are not covered by tests. This information can be used to improve the quality of the documentation by ensuring that all of the markup is tested.

## Prerequisites

To use the `checkMarkupCoverage` function, you will need to have the following:

- A set of files that contain markup.
- A test coverage object that contains information about which lines of code are covered by tests.

## How to use this

To use the `checkMarkupCoverage` function, follow these steps:

1. Import the `checkMarkupCoverage` function into your code.
2. Create a configuration object that specifies the markup types to be analyzed and the file types to be included.
3. Create a test coverage object that contains information about which lines of code are covered by tests.
4. Call the `checkMarkupCoverage` function with the configuration object and the test coverage object as arguments.
5. Use the `markupCoverage` object to identify areas of markup that are not covered by tests.

## Example

The following example shows how to use the `checkMarkupCoverage` function to analyze the markup coverage of a set of Markdown files:

```javascript
const checkMarkupCoverage = require('doc-detective-core/analysis').checkMarkupCoverage;

const config = {
  markupTypes: ['markdown'],
  fileTypes: ['md'],
};

const testCoverage = {
  files: [
    {
      file: 'file1.md',
      coveredLines: [1, 3, 5],
      uncoveredLines: [2, 4],
    },
    {
      file: 'file2.md',
      coveredLines: [1, 3, 5],
      uncoveredLines: [2, 4],
    },
  ],
};

const markupCoverage = checkMarkupCoverage(config, testCoverage);

console.log(markupCoverage);
```

The output of the above example would be a `markupCoverage` object that contains the following information:

```json
{
  summary: {
    covered: 6,
    uncovered: 4,
    markup: {
      markdown: {
        covered: 6,
        uncovered: 4,
      },
    },
  },
  files: [
    {
      file: 'file1.md',
      coveredLines: [1, 3, 5],
      uncoveredLines: [2, 4],
      markup: {
        markdown: {
          coveredLines: [1, 3, 5],
          coveredMatches: [],
          uncoveredLines: [2, 4],
          uncoveredMatches: [],
        },
      },
    },
    {
      file: 'file2.md',
      coveredLines: [1, 3, 5],
      uncoveredLines: [2, 4],
      markup: {
        markdown: {
          coveredLines: [1, 3, 5],
          coveredMatches: [],
          uncoveredLines: [2, 4],
          uncoveredMatches: [],
        },
      },
    },
  ],
  errors: [],
}
```

This information can be used to identify areas of markup that are not covered by tests. In this example, there are four lines of markup that are not covered by tests: lines 2 and 4 in `file1.md` and lines 2 and 4 in `file2.md`.
  
  