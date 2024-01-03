
  
   # **Check Link**

## What does this do?

The `checkLink` method checks if a given URL is valid and returns the HTTP status code.

## Why should I use this?

The `checkLink` method can be used to validate URLs before using them in your code. This can help you avoid errors and ensure that your code is working properly.

## Prerequisites

There are no prerequisites for using the `checkLink` method.

## How to use this

To use the `checkLink` method, you must provide a URL. The URL can be specified as a string or as a `URL` object.

The `checkLink` method also accepts an optional `statusCodes` parameter. This parameter can be used to specify which HTTP status codes should be considered successful. If the `statusCodes` parameter is not specified, the default value is `[200, 201, 202, 203, 204, 205, 206, 300, 301, 302, 303, 304, 305, 307, 308]`.

The `checkLink` method returns a `Promise` that resolves to an object with the following properties:

* `url`: The URL that was checked.
* `statusCodes`: The HTTP status codes that were considered successful.
* `statusCode`: The HTTP status code that was returned by the server.
* `success`: A boolean value that indicates whether the URL is valid.

Here is an example of how to use the `checkLink` method:

```javascript
const url = 'https://www.google.com';

const checkLink = async () => {
  const result = await checkLink(url);

  if (result.success) {
    console.log('The URL is valid.');
  } else {
    console.log('The URL is not valid.');
  }
};

checkLink();
```

## Output

The output of the `checkLink` method is an object with the following properties:

* `url`: The URL that was checked.
* `statusCodes`: The HTTP status codes that were considered successful.
* `statusCode`: The HTTP status code that was returned by the server.
* `success`: A boolean value that indicates whether the URL is valid.

Here is an example of the output of the `checkLink` method:

```json
{
  "url": "https://www.google.com",
  "statusCodes": [200, 201, 202, 203, 204, 205, 206, 300, 301, 302, 303, 304, 305, 307, 308],
  "statusCode": 200,
  "success": true
}
```
  
  