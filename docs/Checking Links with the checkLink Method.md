
  
   # **checkLink**

## What does this do?

The `checkLink` method checks if a given URL is valid and returns an error if it is not.

## Why should I use this?

This method can be used to validate user input, such as when a user enters a URL into a form. It can also be used to check the validity of links in a document or web page.

## Prerequisites

There are no prerequisites for using this method.

## How to use this

To use this method, simply pass the URL you want to check as the first argument. The method will return a Promise that resolves to an object with the following properties:

* `valid`: A boolean value indicating whether the URL is valid.
* `error`: An error object if the URL is not valid.

Here is an example of how to use this method:

```javascript
const checkLink = require('doc-detective-core').checkLink;

checkLink('https://www.google.com')
  .then((result) => {
    if (result.valid) {
      console.log('The URL is valid.');
    } else {
      console.log('The URL is not valid.');
    }
  })
  .catch((error) => {
    console.log('An error occurred while checking the URL.');
  });
```

## Relevant method or class

The following method or class is relevant to this documentation:

* `checkLink` method in the `doc-detective-core` module
  
  