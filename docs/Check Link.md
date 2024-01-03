
  
   # **checkLink**

## What does this do?

The `checkLink` method checks if a given URL is valid and returns the status code of the URL.

## Why should I use this?

This method can be used to check if a URL is valid before attempting to access it. This can be useful for preventing errors and improving the user experience.

## Prerequisites

There are no prerequisites for using this method.

## How to use this

To use this method, simply pass the URL you want to check as the first argument. The method will then return the status code of the URL.

Here is an example of how to use this method:

```
const checkLink = require('doc-detective-core').checkLink;

const url = 'https://www.google.com';

checkLink(url).then((res) => {
  console.log(res.statusCode); // 200
});
```

## Output

The output of this method is a Promise that resolves to an object with the following properties:

* `statusCode`: The status code of the URL.
  
  