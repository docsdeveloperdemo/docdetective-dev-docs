
  
   # **Check Link**

## What does this do?

The `checkLink` method checks if a given URL is valid and returns the HTTP status code.

## Why should I use this?

The `checkLink` method can be used to validate URLs before using them in your code. This can help you to avoid errors and ensure that your code is working properly.

## Prerequisites

There are no prerequisites for using the `checkLink` method.

## How to use this

To use the `checkLink` method, you must provide a URL. The URL can be specified as a string or as a `URL` object.

The `checkLink` method will return a `Promise` that resolves to an object containing the following properties:

* `url`: The URL that was checked.
* `statusCode`: The HTTP status code that was returned by the server.
* `success`: A boolean value indicating whether the URL is valid.

The following code sample shows you how to use the `checkLink` method:

```javascript
const {checkLink} = require('@google-cloud/doc-detective-core');

async function checkLink() {
  const url = 'https://www.google.com';

  const result = await checkLink(url);

  console.log(result);
}

checkLink();
```

## Example

The following code sample shows you how to use the `checkLink` method to check if a URL is valid:

```javascript
const {checkLink} = require('@google-cloud/doc-detective-core');

async function checkLink() {
  const url = 'https://www.google.com';

  const result = await checkLink(url);

  if (result.success) {
    console.log('The URL is valid.');
  } else {
    console.log('The URL is not valid.');
  }
}

checkLink();
```
  
  