
  
   # **httpRequest**

## What does this do?

The `httpRequest` function is a utility function that makes it easy to send HTTP requests. It takes a URL and an optional options object as arguments, and returns a Promise that resolves to the response from the server.

## Why should I use this?

The `httpRequest` function is a convenient way to send HTTP requests without having to worry about the details of the underlying implementation. It also provides a number of features that make it easy to customize the request, such as the ability to set headers, timeouts, and retries.

## Prerequisites

There are no prerequisites for using the `httpRequest` function.

## How to use this

To use the `httpRequest` function, simply call it with the URL of the resource you want to request, and an optional options object. The following example shows how to use the `httpRequest` function to send a GET request to the Google homepage:

```javascript
const httpRequest = require('doc-detective-core/src/tests/httpRequest');

httpRequest('https://www.google.com')
  .then((response) => {
    console.log(response.body);
  })
  .catch((error) => {
    console.error(error);
  });
```

The `httpRequest` function can also be used to send POST, PUT, and DELETE requests. To do this, simply set the `method` property of the options object to the desired HTTP method. The following example shows how to use the `httpRequest` function to send a POST request to the Google homepage:

```javascript
const httpRequest = require('doc-detective-core/src/tests/httpRequest');

httpRequest('https://www.google.com', {
  method: 'POST',
  body: 'Hello, world!'
})
  .then((response) => {
    console.log(response.body);
  })
  .catch((error) => {
    console.error(error);
  });
```

The `httpRequest` function also supports a number of other features, such as the ability to set headers, timeouts, and retries. For more information, see the documentation for the `httpRequest` function.
  
  