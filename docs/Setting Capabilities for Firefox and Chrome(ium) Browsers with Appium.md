
  
   # **getDriverCapabilities**

## What does this do?

The `getDriverCapabilities` function is used to set the capabilities for the Firefox and Chrome(ium) browsers. It takes in a configuration object, a browser name, and an options object, and returns an object containing the capabilities for the specified browser.

## Why should I use this?

You should use this function if you want to use the Firefox or Chrome(ium) browsers with Appium. This function will set the appropriate capabilities for the browser you want to use, so that you can easily start a session and interact with the browser.

## Prerequisites

Before you can use this function, you must have the following prerequisites:

* Appium must be installed and configured.
* The Firefox or Chrome(ium) browser must be installed on your computer.
* The `chromedriver` executable must be installed on your computer (for Chrome(ium) only).

## How to use this

To use this function, simply call it with the following arguments:

* `config`: A configuration object that contains the following properties:
    * `environment`: An object that contains the following properties:
        * `platform`: The platform that you are running Appium on (e.g. "mac", "windows", "linux").
        * `apps`: An array of objects that contain the following properties:
            * `name`: The name of the app.
            * `path`: The path to the app executable.
* `name`: The name of the browser that you want to use (e.g. "firefox", "chrome").
* `options`: An object that contains the following properties:
    * `width`: The width of the browser window.
    * `height`: The height of the browser window.
    * `headless`: A boolean value that indicates whether or not to run the browser in headless mode.
    * `path`: The path to the browser executable (optional).
    * `driverPath`: The path to the `chromedriver` executable (for Chrome(ium) only).

The function will return an object containing the capabilities for the specified browser. You can then use these capabilities to start a session and interact with the browser.

## Example

The following example shows how to use the `getDriverCapabilities` function to set the capabilities for the Firefox browser:

```javascript
const config = {
  environment: {
    platform: "mac",
    apps: [
      {
        name: "firefox",
        path: "/Applications/Firefox.app",
      },
    ],
  },
};

const options = {
  width: 1280,
  height: 800,
  headless: false,
};

const capabilities = getDriverCapabilities(config, "firefox", options);

console.log(capabilities);
```

The output of the above example would be the following:

```json
{
  platformName: "mac",
  "appium:automationName": "Gecko",
  browserName: "MozillaFirefox",
  "moz:firefoxOptions": {
    args: [
      "--width=1280",
      "--height=800",
    ],
    binary: "/Applications/Firefox.app",
  },
}
```
  
  