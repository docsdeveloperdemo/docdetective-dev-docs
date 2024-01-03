
  
   # **checkMarkupCoverage**

## What does this do?

The `checkMarkupCoverage` function analyzes the coverage of markup (e.g., comments, annotations) in a set of files. It takes two parameters:

- `config`: A configuration object that specifies the markup types to be analyzed and the file types to be included.
- `testCoverage`: A test coverage object that contains information about the covered and uncovered lines in each file.

The function returns a `markupCoverage` object that contains the following information:

- A summary of the markup coverage, including the total number of covered and uncovered lines and the coverage percentage for each markup type.
- A list of files, each of which contains information about the covered and uncovered lines and the markup coverage for each markup type.
- A list of errors that occurred during the analysis.

## Why should I use this?

The `checkMarkupCoverage` function can be used to identify areas where the documentation for a set of files is lacking. This information can be used to improve the documentation and ensure that it is complete and accurate.

## Prerequisites

To use the `checkMarkupCoverage` function, you will need the following:

- A set of files to be analyzed.
- A test coverage object that contains information about the covered and uncovered lines in each file.
- The `doc-detective-core` library, which contains the `checkMarkupCoverage` function.

## How to use this

To use the `checkMarkupCoverage` function, follow these steps:

1. Import the `doc-detective-core` library.
2. Create a `config` object that specifies the markup types to be analyzed and the file types to be included.
3. Create a `testCoverage` object that contains information about the covered and uncovered lines in each file.
4. Call the `checkMarkupCoverage` function with the `config` and `testCoverage` objects as parameters.
5. Use the `markupCoverage` object returned by the function to identify areas where the documentation for the set of files is lacking.

## Example

The following example shows how to use the `checkMarkupCoverage` function to analyze the markup coverage of a set of files:

```javascript
const docDetectiveCore = require('doc-detective-core');

// Create a config object that specifies the markup types to be analyzed and the file types to be included.
const config = {
  markupTypes: ['comments', 'annotations'],
  fileTypes: ['js', 'ts']
};

// Create a testCoverage object that contains information about the covered and uncovered lines in each file.
const testCoverage = {
  files: [
    {
      file: 'file1.js',
      coveredLines: [1, 3, 5],
      uncoveredLines: [2, 4]
    },
    {
      file: 'file2.ts',
      coveredLines: [1, 3, 5],
      uncoveredLines: [2, 4]
    }
  ]
};

// Call the checkMarkupCoverage function with the config and testCoverage objects as parameters.
const markupCoverage = docDetectiveCore.checkMarkupCoverage(config, testCoverage);

// Use the markupCoverage object returned by the function to identify areas where the documentation for the set of files is lacking.
console.log(markupCoverage);
```

The output of the above example will be a `markupCoverage` object that contains the following information:

```json
{
  summary: {
    covered: 6,
    uncovered: 4,
    markup: {
      comments: {
        covered: 3,
        uncovered: 2
      },
      annotations: {
        covered: 3,
        uncovered: 2
      }
    }
  },
  files: [
    {
      file: 'file1.js',
      coveredLines: [1, 3, 5],
      uncoveredLines: [2, 4],
      markup: {
        comments: {
          coveredLines: [1, 3],
          uncoveredLines: [2]
        },
        annotations: {
          coveredLines: [5],
          uncoveredLines: [4]
        }
      }
    },
    {
      file: 'file2.ts',
      coveredLines: [1, 3, 5],
      uncoveredLines: [2, 4],
      markup: {
        comments: {
          coveredLines: [1, 3],
          uncoveredLines: [2]
        },
        annotations: {
          coveredLines: [5],
          uncoveredLines: [4]
        }
      }
    }
  ],
  errors: []
}
```

This information can be used to identify areas where the documentation for the set of files is lacking. For example, the above output shows that there are two uncovered comments and two uncovered annotations in the set of files. This information can be used to improve the documentation and ensure that it is complete and accurate.
  
  