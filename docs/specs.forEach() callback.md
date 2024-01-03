
  
   # **Appium Required**

## What does this do?

This code checks if the Appium driver is required for a given test.

## Why should I use this?

This code can be used to determine if the Appium driver is required for a given test. This can be useful for optimizing test execution by only running the Appium driver when it is necessary.

## Prerequisites

None.

## How to use this

To use this code, you can import the `appiumRequired` function from the `doc-detective-core` module. You can then call the `appiumRequired` function with a list of test specifications as an argument. The function will return a boolean value indicating whether or not the Appium driver is required for any of the tests in the list.

Here is an example of how to use the `appiumRequired` function:

```javascript
const { appiumRequired } = require('doc-detective-core');

const specs = [
  {
    contexts: ['NATIVE_APP'],
    tests: [
      {
        contexts: ['NATIVE_APP'],
        steps: [
          {
            action: 'click',
          },
        ],
      },
    ],
  },
];

const appiumRequired = appiumRequired(specs);

console.log(appiumRequired); // true
```

In this example, the `appiumRequired` function is called with a list of test specifications. The first test specification has a context of `NATIVE_APP` and a step that includes the `click` action. The second test specification has a context of `NATIVE_APP` and a step that includes the `click` action. The `appiumRequired` function returns `true` because the Appium driver is required for both of the tests in the list.
  
  