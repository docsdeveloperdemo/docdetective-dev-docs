
  
   # **sanitizePath**

## What does this do?

The `sanitizePath` function takes a file path as input and returns the absolute path to the file if it exists, or `null` if the file does not exist.

## Why should I use this?

The `sanitizePath` function is useful for ensuring that a file exists before attempting to access it. This can help to prevent errors and exceptions from being thrown.

## Prerequisites

There are no prerequisites for using the `sanitizePath` function.

## How to use this

To use the `sanitizePath` function, simply pass the file path as an argument to the function. The function will return the absolute path to the file if it exists, or `null` if the file does not exist.

Here is an example of how to use the `sanitizePath` function:

```javascript
const filepath = '/Users/andrewvanbeek/dev-docs-work/clients/doc-detective-core/src/sanitize.js';
const absolutePath = sanitizePath(filepath);

if (absolutePath) {
  // The file exists, so we can access it
} else {
  // The file does not exist, so we cannot access it
}
```
  
  