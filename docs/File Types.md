
  
   # **File Types**

## What does this do?

This code snippet iterates over the `fileTypes` array and concatenates the `extensions` property of each file type to the `allowedExtensions` array.

## Why should I use this?

This code is used to build a list of allowed file extensions for a specific file type. This list is then used to validate that a file has a valid extension before it is processed.

## Prerequisites

Before using this code, you must have a `fileTypes` array that contains objects with an `extensions` property.

## How to use this

To use this code, you can pass the `fileTypes` array to the `forEach` method of the `config` object. This will iterate over the array and concatenate the `extensions` property of each file type to the `allowedExtensions` array.

Here is an example of how you can use this code:

```javascript
const config = {
  fileTypes: [
    {
      extensions: ['.js', '.jsx']
    },
    {
      extensions: ['.css', '.scss']
    }
  ]
};

config.fileTypes.forEach((fileType) => {
  allowedExtensions = allowedExtensions.concat(fileType.extensions);
});
```

This code will create an `allowedExtensions` array that contains the following values:

```
['.js', '.jsx', '.css', '.scss']
```

This array can then be used to validate that a file has a valid extension before it is processed.
  
  