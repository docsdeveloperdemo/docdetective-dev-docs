
  
   # **setConfig**

## What does this do?

The `setConfig` method is used to set the configuration for the Doc Detective CLI. It takes a configuration object as its argument and validates it before setting the environment variables and loading the configuration.

## Why should I use this?

The `setConfig` method is useful for setting the configuration for the Doc Detective CLI. It allows you to specify the input files, output directory, and other options for the CLI.

## Prerequisites

Before using the `setConfig` method, you must have the Doc Detective CLI installed. You can install the CLI by following the instructions in the [Getting Started](/docs/getting-started) guide.

## How to use this

To use the `setConfig` method, you must first create a configuration object. The configuration object can contain the following properties:

* `envVariables`: An object containing the environment variables that you want to set.
* `input`: An array of strings containing the paths to the input files.
* `output`: The path to the output directory.
* `runTests`: An object containing the options for running tests.
* `environment`: An object containing the current environment.

Once you have created the configuration object, you can pass it to the `setConfig` method. The `setConfig` method will validate the configuration object and set the environment variables and load the configuration.

## Example

The following example shows how to use the `setConfig` method:

```javascript
const config = {
  envVariables: {
    DOC_DETECTIVE_OUTPUT: '/path/to/output/directory',
  },
  input: ['/path/to/input/file1.md', '/path/to/input/file2.md'],
  output: '/path/to/output/directory',
  runTests: {
    input: ['/path/to/test/input/file1.md', '/path/to/test/input/file2.md'],
    setup: ['/path/to/test/setup/file1.js', '/path/to/test/setup/file2.js'],
    cleanup: ['/path/to/test/cleanup/file1.js', '/path/to/test/cleanup/file2.js'],
  },
  environment: {
    apps: ['app1', 'app2'],
  },
};

setConfig(config);
```

## Conclusion

The `setConfig` method is a useful tool for setting the configuration for the Doc Detective CLI. It allows you to specify the input files, output directory, and other options for the CLI.
  
  