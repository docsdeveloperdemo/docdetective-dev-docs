
  
   # **getDefaultContexts**

## What does this do?

The `getDefaultContexts` function is used to generate an array of contexts to run tests against. It first checks if any contexts are defined in the `config.runTests.contexts` array. If so, it checks if each context is supported for the given apps and platform. If a context is supported, it is added to the `contexts` array.

If no contexts are defined in the config, or if none are supported, the function uses a fallback strategy to generate a list of contexts. The fallback strategy uses the first two browsers (`chrome` and `firefox`) that are found in the `config.environment.apps` array. For each browser, the function creates a context object with the browser's name and the platform.

## Why should I use this?

The `getDefaultContexts` function is useful for generating a list of contexts to run tests against. It can be used to ensure that tests are run against all supported contexts, or to customize the list of contexts that are run.

## Prerequisites

Before using the `getDefaultContexts` function, you must have a `config` object that contains the following properties:

* `environment.apps`: An array of app objects. Each app object must have a `name` property.
* `environment.platform`: The platform that the tests will be run on.
* `runTests.contexts`: An array of context objects. Each context object must have an `app` property and a `platforms` property.

## How to use this

To use the `getDefaultContexts` function, simply call it with the `config` object as an argument. The function will return an array of contexts that can be used to run tests against.

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
      {
        app: "chrome",
        platforms: ["windows"],
      },
      {
        app: "firefox",
        platforms: ["windows"],
      },
    ],
  },
};

const contexts = getDefaultContexts(config);

console.log(contexts);
```

The output of the above code would be:

```javascript
[
  {
    app: {
      name: "chrome",
    },
    platforms: ["windows"],
  },
  {
    app: {
      name: "firefox",
    },
    platforms: ["windows"],
  },
]
```
  
  