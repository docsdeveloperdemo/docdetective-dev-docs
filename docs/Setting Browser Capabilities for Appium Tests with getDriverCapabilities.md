
  
   # **getDriverCapabilities**

## What does this do?

The `getDriverCapabilities` function is used to set the capabilities for the Firefox and Chrome browsers when using Appium. It takes in a configuration object, a browser name, and an options object, and returns an object containing the capabilities for the specified browser.

## Why should I use this?

You should use this function if you want to use Appium to automate tests on Firefox or Chrome. By setting the correct capabilities, you can ensure that Appium is able to properly interact with the browser.

## Prerequisites

Before using this function, you must have Appium installed and configured. You must also have the Firefox and Chrome browsers installed on your system.

## How to use this

To use this function, you must first create a configuration object. This object should contain the following properties:

* `environment`: An object containing information about the environment in which you are running your tests. This object should include the following properties:
    * `platform`: The platform on which you are running your tests. This can be either "mac", "windows", or "linux".
    * `apps`: An array of objects containing information about the applications that you want to use in your tests. Each object in this array should include the following properties:
        * `name`: The name of the application.
        * `path`: The path to the application executable.
* `browserName`: The name of the browser that you want to use. This can be either "firefox" or "chrome".
* `options`: An object containing additional options for the browser. This object can include the following properties:
    * `width`: The width of the browser window.
    * `height`: The height of the browser window.
    * `headless`: A boolean value indicating whether or not to run the browser in headless mode.
    * `path`: The path to the browser executable.
    * `driverPath`: The path to the Appium driver executable.

Once you have created the configuration object, you can call the `getDriverCapabilities` function to get the capabilities for the specified browser. The function will return an object containing the following properties:

* `platformName`: The platform on which the browser is running.
* `appium:automationName`: The automation name for the browser.
* `browserName`: The name of the browser.
* `moz:firefoxOptions` (for Firefox): An object containing additional options for Firefox.
* `goog:chromeOptions` (for Chrome): An object containing additional options for Chrome.

You can then use these capabilities to create an Appium driver and start your tests.

## Example

The following example shows how to use the `getDriverCapabilities` function to set the capabilities for Firefox and Chrome:

```javascript
const config = {
  environment: {
    platform: "mac",
    apps: [
      {
        name: "firefox",
        path: "/Applications/Firefox.app",
      },
      {
        name: "chrome",
        path: "/Applications/Google Chrome.app",
      },
      {
        name: "chromedriver",
        path: "/usr/local/bin/chromedriver",
      },
    ],
  },
  browserName: "firefox",
  options: {
    width: 1280,
    height: 800,
    headless: false,
  },
};

const capabilities = getDriverCapabilities(config, "firefox", options);

// Create an Appium driver and start your tests
```
  
  