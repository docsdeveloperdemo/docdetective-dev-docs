
  
   # **buildRunShell**

## What does this do?

The `buildRunShell` function constructs a `runShell` action object, which can be used to execute a shell command on the user's machine.

## Why should I use this?

The `buildRunShell` function is useful for executing shell commands that are not available as built-in actions in the Doc Detective Core library. For example, you could use the `buildRunShell` function to execute a custom script that performs a specific task, such as generating a report or deploying a website.

## Prerequisites

To use the `buildRunShell` function, you must have the following prerequisites:

* Node.js installed on your machine
* The Doc Detective Core library installed in your project

## How to use this

To use the `buildRunShell` function, follow these steps:

1. Import the Doc Detective Core library into your project.
2. Call the `buildRunShell` function with the following parameters:
    * `config`: A configuration object that contains the following properties:
        * `cwd`: The current working directory for the shell command
        * `env`: The environment variables for the shell command
    * `match`: A match object that contains the text that triggered the action

The `buildRunShell` function will return an action object that can be used to execute the shell command.

## Example

The following example shows how to use the `buildRunShell` function to execute a shell command:

```javascript
const docDetectiveCore = require('doc-detective-core');

const config = {
  cwd: '/Users/andrewvanbeek/dev-docs-work/clients/doc-detective-core',
  env: {
    NODE_ENV: 'development'
  }
};

const match = {
  text: 'run the following command: ls -la'
};

const action = docDetectiveCore.buildRunShell(config, match);

action.execute();
```

This example will execute the `ls -la` command in the `/Users/andrewvanbeek/dev-docs-work/clients/doc-detective-core` directory.
  
  