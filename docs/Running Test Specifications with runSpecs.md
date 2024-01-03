
  
   # **runSpecs**

## What does this do?

The `runSpecs` function is the entry point for running a set of test specifications (`specs`) in a given configuration (`config`). It performs the following tasks:

- Sets up initial shorthand values, including default contexts, platform, and available applications.
- Determines which applications are required for the specified tests.
- Warms up Appium and OBS (if required).
- Iterates through the test specifications and tests, executing each test in a specified context.
- Parses the results of each step, context, and test to determine the overall result.
- Closes the Appium server.

## Why should I use this?

The `runSpecs` function provides a convenient way to run a set of test specifications in a specified configuration. It handles the setup, execution, and reporting of test results, making it easier to automate and manage testing processes.

## Prerequisites

To use the `runSpecs` function, you will need the following:

- A set of test specifications (`specs`) in the correct format.
- A configuration (`config`) that specifies the environment and options for running the tests.
- Appium and OBS (if required) installed and configured.

## How to use this

To use the `runSpecs` function, simply call it with the appropriate configuration and test specifications:

```
const report = await runSpecs(config, specs);
```

The `report` object will contain the results of the test run, including the status of each step, context, and test, as well as summary statistics.

Here is an example of how the `runSpecs` function can be used in a Node.js script:

```
const { runSpecs } = require('doc-detective-core');

const config = {
  environment: {
    platform: 'windows',
    apps: [
      { name: 'MyApp', path: '/path/to/myApp.apk' },
    ],
  },
};

const specs = [
  {
    id: 'spec1',
    tests: [
      {
        id: 'test1',
        steps: [
          {
            id: 'step1',
            action: 'click',
            target: '#button1',
          },
        ],
      },
    ],
  },
];

const report = await runSpecs(config, specs);

console.log(report);
```

This script will run the specified test specification in the given configuration and print the results to the console.
  
  