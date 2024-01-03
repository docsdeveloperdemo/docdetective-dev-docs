
  
   # **Appium Is Ready**

## What does this do?

The `appiumIsReady` function checks if the Appium server is ready to receive commands. It does this by sending a GET request to the Appium server's `/sessions` endpoint. If the server responds with a 200 status code, the function returns `true`. Otherwise, it retries the request after a configurable delay.

## Why should I use this?

You should use this function to ensure that the Appium server is ready before sending any commands to it. This will help to prevent errors and ensure that your tests run smoothly.

## Prerequisites

Before using this function, you must have the following:

* An Appium server running on port 4723
* The `axios` library installed

## How to use this

To use this function, simply call it and pass it the URL of the Appium server's `/sessions` endpoint. The function will return a Promise that resolves to `true` if the server is ready or `false` if the server is not ready.

Here is an example of how to use this function:

```javascript
const appiumIsReady = require('doc-detective-core/src/tests.js');

appiumIsReady('http://0.0.0.0:4723/sessions').then((isReady) => {
  if (isReady) {
    // The Appium server is ready. You can now send commands to it.
  } else {
    // The Appium server is not ready. You should wait a bit and try again.
  }
});
```
  
  