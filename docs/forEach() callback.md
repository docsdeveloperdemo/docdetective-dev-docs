
  
   # **File System Utilities**

## What does this do?

The `utils.js` file contains a collection of utility functions that are used throughout the Doc Detective core library. These functions provide various functionalities such as reading files and directories, checking file types, and filtering files based on specific criteria.

## Why should I use this?

The utility functions in this file can be useful for developers who are working on projects that involve reading and processing files and directories. These functions can help to simplify and streamline common file-related tasks, making it easier to write efficient and maintainable code.

## Prerequisites

To use the utility functions in this file, you will need to have Node.js installed on your system. You will also need to have the `fs` module installed, which is a core Node.js module that provides file system-related functionality.

## How to use this

To use the utility functions in this file, you can import them into your own code using the following syntax:

```javascript
const { readdirSync, statSync, isFile, isDir } = require('doc-detective-core/src/utils');
```

Once you have imported the utility functions, you can use them in your code as needed. For example, the following code uses the `readdirSync` function to read the contents of a directory:

```javascript
const files = readdirSync('path/to/directory');
```

The `statSync` function can be used to check the file type of a file or directory:

```javascript
const isFile = statSync('path/to/file').isFile();
const isDir = statSync('path/to/directory').isDirectory();
```

The `isFile` and `isDir` functions can be used to filter files and directories based on their type:

```javascript
const files = readdirSync('path/to/directory').filter(isFile);
const dirs = readdirSync('path/to/directory').filter(isDir);
```

## Conclusion

The utility functions in the `utils.js` file can be a valuable resource for developers who are working on projects that involve reading and processing files and directories. These functions can help to simplify and streamline common file-related tasks, making it easier to write efficient and maintainable code.
  
  