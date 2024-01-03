
  
   # **File Type Extensions**

## What does this do?

This code snippet collects all the file extensions from the `config.fileTypes` object and adds them to the `allowedExtensions` array.

## Why should I use this?

This is useful for checking if a file has a valid extension before processing it.

## Prerequisites

There are no prerequisites for using this code.

## How to use this

To use this code, simply import the `utils` module and call the `getFileExtensions` function. The function will return an array of all the allowed file extensions.

Here is an example of how to use this code:

```javascript
const utils = require('./utils');

const allowedExtensions = utils.getFileExtensions();

console.log(allowedExtensions);
```

Output:

```
[ '.js', '.css', '.html' ]
```
  
  