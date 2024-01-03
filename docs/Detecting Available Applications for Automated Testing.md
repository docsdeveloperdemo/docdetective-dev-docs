
  
   # **getAvailableApps**

## What does this do?

The `getAvailableApps` function detects and returns a list of available applications that can be used for testing. These applications include Chrome, Chromium, Firefox, Edge, Safari, Android Studio, iOS Simulator, and OBS.

## Why should I use this?

The `getAvailableApps` function is useful for setting up and running automated tests that require specific applications to be installed and accessible. By using this function, you can ensure that the necessary applications are available and ready for testing, reducing the risk of test failures due to missing dependencies.

## Prerequisites

Before using the `getAvailableApps` function, you must have the following prerequisites in place:

- Node.js and npm installed on your system.
- The `@eyeo/get-browser-binary` package installed as a dependency.
- The `chromedriver` package installed as a dependency.

## How to use this

To use the `getAvailableApps` function, simply import it into your code and call it with the appropriate configuration object. The configuration object should include the following properties:

- `environment.platform`: The platform on which the tests will be run (e.g. "windows", "linux", "darwin").

The `getAvailableApps` function will return an array of objects, each representing an available application. Each application object will have the following properties:

- `name`: The name of the application (e.g. "chrome", "firefox").
- `path`: The path to the application executable (e.g. "/Applications/Google Chrome.app").

You can use the information provided by the `getAvailableApps` function to launch and control the desired applications for your automated tests.

## Example

The following code shows an example of how to use the `getAvailableApps` function:

```javascript
const { getAvailableApps } = require('@doc-detective/core');

const config = {
  environment: {
    platform: 'windows'
  }
};

const apps = getAvailableApps(config);

console.log(apps);
```

The output of the above code will be an array of objects representing the available applications on the Windows platform.
  
  