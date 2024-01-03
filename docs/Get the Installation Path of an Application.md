
  
   # **getInstallPath**

## What does this do?

The `getInstallPath` function returns the installation path of a given application.

## Why should I use this?

This function can be used to find the installation path of an application, which can be useful for a variety of purposes, such as:

* Launching the application
* Updating the application
* Uninstalling the application

## Prerequisites

Before using the `getInstallPath` function, you must have the following:

* The name of the application you want to find the installation path for
* The platform that the application is installed on (e.g. "mac", "linux", "windows")

## How to use this

To use the `getInstallPath` function, simply call the function with the following arguments:

* `config`: A configuration object that contains the platform of the application you want to find the installation path for
* `id`: The name of the application you want to find the installation path for

The function will return the installation path of the application, or an empty string if the application is not found.

## Example

The following example shows how to use the `getInstallPath` function to find the installation path of the "Google Chrome" application on a Mac:

```javascript
const config = {
  environment: {
    platform: "mac"
  }
};

const id = "Google Chrome";

const installPath = getInstallPath(config, id);

console.log(installPath);
```

The output of the above example will be the installation path of the "Google Chrome" application on the Mac.
  
  