
  
   # **Check Link**

## What does this do?

The `checkLink` method checks if a given URL returns a valid HTTP status code.

## Why should I use this?

This method can be used to validate that a URL is valid and accessible, and to ensure that it returns the expected HTTP status code. This can be useful for testing web applications and APIs, or for monitoring the availability of external resources.

## Prerequisites

To use the `checkLink` method, you will need to have the following:

* A valid URL to check.
* A list of expected HTTP status codes.

## How to use this

To use the `checkLink` method, simply call the method with the following parameters:

* `url`: The URL to check.
* `statusCodes`: A list of expected HTTP status codes.

The method will return a result object with the following properties:

* `status`: The status of the request. This can be either "PASS" or "FAIL".
* `description`: A description of the result. This will include the HTTP status code that was returned, and any errors that occurred.

Here is an example of how to use the `checkLink` method:

```
const result = await checkLink("https://www.google.com", [200]);

if (result.status === "PASS") {
  console.log("The URL is valid and accessible.");
} else {
  console.log("The URL is invalid or inaccessible.");
}
```

## Additional notes

* The `checkLink` method can be used to check any type of URL, including HTTP, HTTPS, and FTP URLs.
* The method will automatically follow redirects.
* The method will timeout after 10 seconds.
* The method can be used in both synchronous and asynchronous code.
  
  