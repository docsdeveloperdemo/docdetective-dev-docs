
  
   # **getDefaultContexts**

## What does this do?

The `getDefaultContexts` function is used to generate a list of contexts to run tests against. It first checks if any contexts are defined in the `config.runTests.contexts` array. If so, it checks if each context is supported for the given apps and platform. If a context is supported, it is added to the list of contexts.

If no contexts are defined in the config, or if none are supported, the function uses a fallback strategy to generate a list of contexts. The fallback strategy uses the first two browsers (`chrome` and `firefox`) that are found in the `config.environment.apps` array. For each browser, the function creates a context object with the browser's name and the platform.

## Why should I use this?

The `getDefaultContexts` function is useful for generating a list of contexts to run tests against without having to manually specify each context. This can be helpful when you want to run tests against multiple browsers or platforms.

## Prerequisites

Before using the `getDefaultContexts` function, you must have the following:

* A `config` object that contains the following properties:
    * `environment.apps`: An array of app objects. Each app object must have a `name` property.
    * `environment.platform`: The platform to run tests against.
    * `runTests.contexts`: An array of context objects. Each context object must have a `name` property.

## How to use this

To use the `getDefaultContexts` function, simply call the function with the `config` object as the argument. The function will return an array of context objects.

Here is an example of how to use the `getDefaultContexts` function:

```javascript
const config = {
  environment: {
    apps: [
      {
        name: "chrome",
      },
      {
        name: "firefox",
      },
    ],
    platform: "windows",
  },
  runTests: {
    contexts: [
      "chrome",
      "firefox",
    ],
  },
};

const contexts = getDefaultContexts(config);

console.log(contexts);
```

The output of the above code will be an array of two context objects:

```json
[
  {
    app: {
      name: "chrome",
    },
    platforms: [
      "windows",
    ],
  },
  {
    app: {
      name: "firefox",
    },
    platforms: [
      "windows",
    ],
  },
]
```
  
  