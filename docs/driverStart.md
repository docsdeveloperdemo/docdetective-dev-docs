
  
   # **driverStart**

## What does this do?

The `driverStart` function is used to start a WebDriver session with the specified capabilities.

## Why should I use this?

You should use this function if you want to automate a web browser using WebDriver.

## Prerequisites

Before you can use this function, you must have the following installed:

* Node.js
* WebDriver

## How to use this

To use this function, you must first create a WebDriver client. You can do this by using the `wdio.remote` function. The following code shows you how to create a WebDriver client:

```javascript
const wdio = require("webdriverio");

const driver = await wdio.remote({
  protocol: "http",
  hostname: "0.0.0.0",
  port: 4723,
  path: "/",
  capabilities,
});
```

Once you have created a WebDriver client, you can use the `driverStart` function to start a WebDriver session. The following code shows you how to start a WebDriver session:

```javascript
const driver = await driverStart(capabilities);
```

The `driverStart` function will return a WebDriver session object. You can use this object to interact with the web browser.

## Example

The following code shows you how to use the `driverStart` function to automate a web browser:

```javascript
const wdio = require("webdriverio");

const driver = await wdio.remote({
  protocol: "http",
  hostname: "0.0.0.0",
  port: 4723,
  path: "/",
  capabilities,
});

await driver.get("https://www.google.com");

const title = await driver.getTitle();

console.log(title);

await driver.quit();
```

This code will open the Google homepage in a web browser and then print the title of the page to the console.
  
  