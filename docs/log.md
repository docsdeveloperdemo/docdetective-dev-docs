
  
   # **Log**

## What does this do?

The `log` function is a utility function that logs messages to the console based on a specified log level. It takes three parameters:

- `config`: An object containing the log level configuration.
- `level`: The log level of the message.
- `message`: The message to log.

## Why should I use this?

The `log` function provides a consistent way to log messages to the console, making it easier to debug and troubleshoot your code. It also allows you to control the level of detail that is logged, so that you can avoid logging unnecessary information.

## Prerequisites

There are no prerequisites for using the `log` function.

## How to use this

To use the `log` function, simply call it with the appropriate parameters. For example, the following code logs an error message to the console:

```javascript
log({ logLevel: "error" }, "error", "An error occurred.");
```

You can also log objects to the console by passing them as the `message` parameter. For example, the following code logs an object to the console:

```javascript
log({ logLevel: "info" }, "info", {
  name: "John Doe",
  age: 30
});
```

## Relevant method or class

The `log` function is a utility function that is not specific to any particular method or class. However, it can be used in conjunction with any method or class that needs to log messages to the console.

## Example

The following example shows how to use the `log` function to log messages to the console from a Node.js script:

```javascript
// Import the log function
const { log } = require("./utils");

// Log an error message
log({ logLevel: "error" }, "error", "An error occurred.");

// Log an info message
log({ logLevel: "info" }, "info", {
  name: "John Doe",
  age: 30
});
```
  
  