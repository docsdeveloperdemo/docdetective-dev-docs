
  
   # **File Type Detection**

## What does this do?

The `fileType` function detects the file type of a file based on its extension. It takes a file extension as an argument and returns the corresponding file type object.

## Why should I use this?

The `fileType` function can be used to determine the type of a file before processing it. This can be useful for tasks such as:

* Opening the file in the correct application
* Converting the file to a different format
* Applying the appropriate security measures

## Prerequisites

There are no prerequisites for using the `fileType` function.

## How to use this

To use the `fileType` function, simply pass the file extension as an argument to the function. The function will return the corresponding file type object.

For example, the following code would return the file type object for a file with the extension `.txt`:

```javascript
const fileType = require('doc-detective-core/utils').fileType;

const txtFileType = fileType('.txt');

console.log(txtFileType); // { name: 'Text', extensions: ['.txt'] }
```

## Gotchas

* The `fileType` function only supports a limited number of file extensions. If the file extension is not recognized, the function will return `null`.
* The `fileType` function does not take into account the file's contents. It is possible for a file to have an incorrect extension.
  
  