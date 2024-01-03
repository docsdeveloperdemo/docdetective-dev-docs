
  
   # **checkLink**

## What does this do?

The `checkLink` method checks if a given URL returns a specific status code.

## Why should I use this?

This method can be used to verify that a URL is responding as expected. For example, you could use it to check that a web server is up and running, or that a specific API endpoint is returning the correct status code.

## Prerequisites

There are no prerequisites for using the `checkLink` method.

## How to use this

To use the `checkLink` method, you must provide the following parameters:

* `url`: The URL to check.
* `statusCodes`: An array of expected status codes.

The `checkLink` method will return a result object with the following properties:

* `status`: A string indicating the status of the request. This will be either "PASS" or "FAIL".
* `description`: A string describing the result of the request.

Here is an example of how to use the `checkLink` method:

```javascript
const result = await checkLink({
  url: "https://www.google.com",
  statusCodes: [200]
});

if (result.status === "PASS") {
  console.log("The URL is responding as expected.");
} else {
  console.log("The URL is not responding as expected.");
}
```

## Additional notes

* The `checkLink` method will automatically add the "https://" protocol to the URL if it is not already present.
* The `checkLink` method will automatically prepend the `origin` property to the URL if it is set.
* The `checkLink` method will validate the step payload before performing the request. If the payload is invalid, the method will return a result object with the status "FAIL" and a description indicating the error.
  
  