
  
   # **Check Markup Coverage**

## What does this do?

The `checkMarkupCoverage` function analyzes the coverage of markup (e.g., Markdown, HTML, etc.) within a set of files. It identifies which markup elements are covered by test coverage and which are not.

## Why should I use this?

Using `checkMarkupCoverage` can help you ensure that your documentation is well-tested and that all markup elements are accounted for in your test coverage. This can help you identify areas where your documentation may be lacking or incomplete.

## Prerequisites

To use `checkMarkupCoverage`, you will need the following:

- A set of files to analyze
- A test coverage report for the files

## How to use this

To use `checkMarkupCoverage`, follow these steps:

1. Import the `checkMarkupCoverage` function from the `doc-detective-core` library.
2. Call the `checkMarkupCoverage` function with the following parameters:
    - `config`: A configuration object that specifies the markup types to be analyzed.
    - `testCoverage`: A test coverage report for the files.
3. The function will return a coverage report that includes the following information:
    - A summary of the coverage of all markup types
    - A list of files with their coverage details
    - A list of errors encountered during the analysis

## Example

The following example shows how to use the `checkMarkupCoverage` function:

```javascript
const { checkMarkupCoverage } = require('doc-detective-core');

const config = {
  markupTypes: ['markdown', 'html']
};

const testCoverage = {
  files: [
    {
      file: 'file1.md',
      coveredLines: [1, 2, 3],
      uncoveredLines: [4, 5, 6],
      fileType: {
        markup: [
          {
            name: 'markdown',
            regex: [
              /^\s*#+\s+(.+)/,
              /^\s*\*\*(.+)\*\*/,
              /^\s*```(.+)```/
            ]
          }
        ]
      }
    }
  ]
};

const coverageReport = checkMarkupCoverage(config, testCoverage);

console.log(coverageReport);
```

The output of the above example will be a coverage report that includes the following information:

```json
{
  summary: {
    covered: 3,
    uncovered: 3,
    markup: {
      markdown: {
        covered: 3,
        uncovered: 3
      }
    }
  },
  files: [
    {
      file: 'file1.md',
      coveredLines: [1, 2, 3],
      uncoveredLines: [4, 5, 6],
      markup: {
        markdown: {
          coveredLines: [1, 2, 3],
          coveredMatches: [],
          uncoveredLines: [4, 5, 6],
          uncoveredMatches: []
        }
      }
    }
  ],
  errors: []
}
```
  
  