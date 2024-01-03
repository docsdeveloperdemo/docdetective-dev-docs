
  
   # **getAvailableApps**

## What does this do?

The `getAvailableApps` function detects and returns a list of available applications that can be used for testing. These applications include Chrome, Chromium, Firefox, Edge, Safari, Android Studio, iOS Simulator, and OBS.

## Why should I use this?

The `getAvailableApps` function is useful for setting up and running automated tests that require specific applications to be installed and accessible. By using this function, you can easily detect and use the available applications without having to manually check for their installation or configuration.

## Prerequisites

Before using the `getAvailableApps` function, you must ensure that the following prerequisites are met:

- Node.js and npm are installed on your system.
- The `@eyeo/get-browser-binary` package is installed.
- The `chromedriver` package is installed.

## How to use this

To use the `getAvailableApps` function, simply import it into your JavaScript file and call it with the following parameters:

```javascript
const { getAvailableApps } = require('@doc-detective/core');

const apps = await getAvailableApps(config);
```

The `config` parameter is an object that contains information about the environment in which the function is running. The following properties are supported:

- `environment.platform`: The platform on which the function is running (e.g. "windows", "linux", "darwin").
- `environment.arch`: The architecture of the platform (e.g. "x64", "arm64").

The `getAvailableApps` function will return an array of objects, each representing an available application. Each object will have the following properties:

- `name`: The name of the application (e.g. "chrome", "firefox").
- `path`: The path to the application executable (e.g. "/Applications/Google Chrome.app").

## Example

The following example shows how to use the `getAvailableApps` function to detect and use available applications for testing:

```javascript
const { getAvailableApps } = require('@doc-detective/core');

const apps = await getAvailableApps(config);

for (const app of apps) {
  // Use the app for testing
}
```

## Conclusion

The `getAvailableApps` function is a useful tool for detecting and using available applications for testing. By using this function, you can easily set up and run automated tests that require specific applications to be installed and accessible.
  
  