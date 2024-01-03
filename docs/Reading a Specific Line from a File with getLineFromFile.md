
  
   # **get-line-from-file**

## What does this do?

The `getLineFromFile` function reads a specified line from a file and returns it as a string.

## Why should I use this?

This function is useful when you need to access a specific line of text from a file, such as a configuration file or a log file.

## Prerequisites

To use this function, you will need to have the following:

* The path to the file you want to read from
* The line number of the line you want to read

## How to use this

To use this function, simply call it with the following arguments:

* `filepath`: The path to the file you want to read from
* `line`: The line number of the line you want to read

The function will return the specified line of text as a string.

## Example

The following example shows how to use the `getLineFromFile` function to read the first line of a file:

```javascript
const line = getLineFromFile('/path/to/file.txt', 1);
```

The variable `line` will now contain the first line of the file `/path/to/file.txt`.
  
  