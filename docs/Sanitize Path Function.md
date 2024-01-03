
  
   # **sanitizePath**

## What does this do?

The `sanitizePath` function takes a file path as an argument and returns the absolute path to the file if it exists, or `null` if it does not.

## Why should I use this?

The `sanitizePath` function can be used to ensure that a file exists before attempting to access it. This can be useful for preventing errors and ensuring that your code runs smoothly.

## Prerequisites

There are no prerequisites for using the `sanitizePath` function.

## How to use this

To use the `sanitizePath` function, simply pass the file path as an argument to the function. The function will return the absolute path to the file if it exists, or `null` if it does not.

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

## Additional information

The `sanitizePath` function can also be used to check if a directory exists. To do this, simply pass the directory path as an argument to the function. The function will return the absolute path to the directory if it exists, or `null` if it does not.

Here is an example of how to use the `sanitizePath` function to check if a directory exists:

```javascript
const directoryPath = '/Users/andrewvanbeek/dev-docs-work/clients/doc-detective-core/src';
const absolutePath = sanitizePath(directoryPath);

if (absolutePath) {
  // The directory exists, so we can access it
} else {
  // The directory does not exist, so we cannot access it
}
```
  
  