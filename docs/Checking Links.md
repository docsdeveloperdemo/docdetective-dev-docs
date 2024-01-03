
  
   # **Check Link**

## What does this do?

The `checkLink` method checks if a given URL is valid and returns the HTTP status code.

## Why should I use this?

The `checkLink` method can be used to validate URLs before using them in your code. This can help you to avoid errors and ensure that your code is working properly.

## Prerequisites

There are no prerequisites for using the `checkLink` method.

## How to use this

To use the `checkLink` method, you must provide a URL. The URL can be specified as a string or as a `URL` object.

The `checkLink` method will return a `Promise` that resolves to an object with the following properties:

* `url`: The URL that was checked.
* `statusCode`: The HTTP status code of the URL.
* `success`: A boolean value indicating whether the URL is valid.

The following code sample shows you how to use the `checkLink` method:

```js
const url = 'https://www.google.com';

checkLink(url).then((result) => {
  console.log(result);
});
```

The output of the code sample will be:

```json
{
  "url": "https://www.google.com",
  "statusCode": 200,
  "success": true
}
```

## Additional information

The `checkLink` method can also be used to check the status of a URL that is behind a firewall or proxy. To do this, you must provide the username and password for the firewall or proxy.

The following code sample shows you how to use the `checkLink` method to check the status of a URL that is behind a firewall or proxy:

```js
const url = 'https://www.google.com';
const username = 'myUsername';
const password = 'myPassword';

checkLink(url, username, password).then((result) => {
  console.log(result);
});
```

The output of the code sample will be:

```json
{
  "url": "https://www.google.com",
  "statusCode": 200,
  "success": true
}
```
  
  