
  
   # **sanitizePath**

## What does this do?

The `sanitizePath` function takes a file path as an argument and returns the absolute path to the file if it exists, or `null` if it does not.

## Why should I use this?

This function is useful for ensuring that a file exists before attempting to access it. This can help to prevent errors and exceptions from being thrown.

## Prerequisites

There are no prerequisites for using this function.

## How to use this

To use this function, simply pass the file path as an argument to the function and it will return the absolute path to the file if it exists, or `null` if it does not.

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

The `sanitizePath` function uses the `path.resolve()` function to convert the relative file path to an absolute file path. The `fs.existsSync()` function is then used to check if the file exists.
  
  