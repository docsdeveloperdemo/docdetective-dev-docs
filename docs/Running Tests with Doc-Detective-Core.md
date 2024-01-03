
  
   # **runTests**

## What does this do?

The `runTests` function is the entry point for running tests using the `doc-detective-core` library. It sets up the configuration, files, and test specifications, and then runs the tests and returns the results.

## Why should I use this?

The `runTests` function is a convenient way to run tests using the `doc-detective-core` library. It handles all of the setup and configuration, so you can focus on writing your tests.

## Prerequisites

Before you can use the `runTests` function, you must install the `doc-detective-core` library. You can do this by running the following command:

```
npm install doc-detective-core
```

## How to use this

To use the `runTests` function, you must provide a configuration object. The configuration object can contain the following properties:

* `files`: An array of file paths to be tested.
* `specs`: An array of test specifications.
* `config`: A configuration object that can contain any additional properties you want to pass to the `runTests` function.

The following is an example of a configuration object:

```
const config = {
  files: ['src/**/*.js'],
  specs: ['test/**/*.js'],
  config: {
    // Additional configuration properties
  }
};
```

Once you have created a configuration object, you can call the `runTests` function as follows:

```
const results = await runTests(config);
```

The `runTests` function will return an array of test results. Each test result will contain the following properties:

* `name`: The name of the test.
* `status`: The status of the test (either "pass" or "fail").
* `message`: A message describing the test result.

The following is an example of a test result:

```
{
  name: 'My test',
  status: 'pass',
  message: 'The test passed.'
}
```

## Conclusion

The `runTests` function is a convenient way to run tests using the `doc-detective-core` library. It handles all of the setup and configuration, so you can focus on writing your tests.
  
  