
  
   # **File Type**

## What does this do?

The `fileType` constant is used to find the file type that corresponds to the given file extension. This is done by iterating over the list of file types and checking if the extension is included in the list of extensions for each file type.

## Why should I use this?

The `fileType` constant is useful for determining the type of file that is being processed. This information can be used to perform different operations on the file, such as opening it with the appropriate application or converting it to a different format.

## Prerequisites

There are no prerequisites for using the `fileType` constant.

## How to use this

To use the `fileType` constant, simply import it from the `doc-detective-core` module and then use it to find the file type that corresponds to the given file extension.

```javascript
const { fileType } = require('doc-detective-core');

const extension = 'txt';
const fileType = fileType.find((fileType) => fileType.extensions.includes(extension));

console.log(fileType); // { name: 'Text File', extensions: ['.txt'] }
```
  
  