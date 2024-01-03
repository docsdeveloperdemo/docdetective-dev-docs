
  
   # **Check Markup Coverage**

## What does this do?

The `checkMarkupCoverage` function analyzes the coverage of markup (e.g., Markdown, HTML, etc.) within a set of files. It identifies which markup elements are covered by test coverage and which are not.

## Why should I use this?

Using `checkMarkupCoverage` can help you ensure that your documentation is well-tested and that all markup elements are accounted for in your test suite. This can improve the overall quality and reliability of your documentation.

## Prerequisites

To use `checkMarkupCoverage`, you will need the following:

- A set of files to analyze
- A test coverage report that includes line coverage information

## How to use this

To use `checkMarkupCoverage`, follow these steps:

1. Import the `checkMarkupCoverage` function into your code.
2. Call the `checkMarkupCoverage` function, passing in the following parameters:
    - `config`: A configuration object that specifies the markup types to analyze and the test coverage report to use.
    - `testCoverage`: A test coverage report that includes line coverage information.
3. The `checkMarkupCoverage` function will return a coverage report that includes the following information:
    - A summary of the overall coverage of markup elements
    - A list of files with coverage information for each file
    - A list of errors that occurred during the analysis

## Example

The following example shows how to use the `checkMarkupCoverage` function to analyze the coverage of Markdown elements in a set of files:

```javascript
const checkMarkupCoverage = require('doc-detective-core/analysis').checkMarkupCoverage;

const config = {
  markupTypes: ['markdown'],
  testCoverageReport: 'coverage.json'
};

const testCoverage = require(config.testCoverageReport);

const coverageReport = checkMarkupCoverage(config, testCoverage);

console.log(coverageReport);
```

The output of the `checkMarkupCoverage` function will be a JSON object that contains the following information:

```json
{
  "summary": {
    "covered": 10,
    "uncovered": 5,
    "markup": {
      "markdown": {
        "covered": 10,
        "uncovered": 5
      }
    }
  },
  "files": [
    {
      "file": "file1.md",
      "coveredLines": [1, 2, 3, 4, 5],
      "uncoveredLines": [6, 7, 8, 9, 10],
      "markup": {
        "markdown": {
          "coveredLines": [1, 2, 3, 4, 5],
          "coveredMatches": [
            {
              "line": 1,
              "indexInFile": 10,
              "text": "This is a header"
            },
            {
              "line": 2,
              "indexInFile": 20,
              "text": "This is a paragraph"
            }
          ],
          "uncoveredLines": [6, 7, 8, 9, 10],
          "uncoveredMatches": [
            {
              "line": 6,
              "indexInFile": 30,
              "text": "This is an uncovered line"
            }
          ]
        }
      }
    }
  ],
  "errors": []
}
```

This coverage report shows that there are 10 covered Markdown elements and 5 uncovered Markdown elements in the set of files. It also provides detailed information about the coverage of each file and each markup type.
  
  