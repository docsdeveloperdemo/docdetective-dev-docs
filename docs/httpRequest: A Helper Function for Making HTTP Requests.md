
  
   # **httpRequest**

## What does this do?

The `httpRequest` function is a helper function that makes it easy to make HTTP requests. It takes a URL and a set of options as arguments, and returns a Promise that resolves to the response from the server.

## Why should I use this?

The `httpRequest` function is a convenient way to make HTTP requests without having to worry about the details of the underlying implementation. It also provides a number of features that make it easy to customize the behavior of the request, such as the ability to set timeouts, add headers, and follow redirects.

## Prerequisites

In order to use the `httpRequest` function, you must have a valid URL and a set of options. The options object can contain any of the following properties:

* `method`: The HTTP method to use, such as "GET", "POST", "PUT", or "DELETE".
* `headers`: An object containing the headers to send with the request.
* `body`: The body of the request, as a string or a Buffer.
* `timeout`: The maximum amount of time to wait for the server to respond, in milliseconds.
* `followRedirects`: A boolean value indicating whether or not to follow redirects.

## How to use this

To use the `httpRequest` function, simply call it with the URL and a set of options. The function will return a Promise that resolves to the response from the server.

Here is an example of how to use the `httpRequest` function to make a GET request to the Google homepage:

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

## Conclusion

The `httpRequest` function is a powerful tool that can be used to make HTTP requests easily and efficiently. It is a great choice for developers who need to make HTTP requests as part of their applications.
  
  