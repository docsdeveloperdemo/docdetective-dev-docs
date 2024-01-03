
  
   # **spawnCommand**

## What does this do?

The `spawnCommand` function executes a command in the operating system's shell and returns the standard output, standard error, and exit code of the command.

## Why should I use this?

The `spawnCommand` function is useful for running external commands from within a Node.js script. This can be useful for tasks such as running system commands, interacting with other programs, or automating tasks.

## Prerequisites

To use the `spawnCommand` function, you must have the `child_process` module installed. You can install the `child_process` module using the following command:

```
npm install child_process
```

## How to use this

To use the `spawnCommand` function, you must provide the following arguments:

* `cmd`: The command to execute.
* `args`: An array of arguments to pass to the command.
* `options`: An object of options to pass to the `spawn` function.

The following example shows how to use the `spawnCommand` function to execute the `ls` command:

```
const { spawnCommand } = require('doc-detective-core');

const { stdout, stderr, exitCode } = await spawnCommand('ls', ['-l']);

console.log(stdout);
console.log(stderr);
console.log(exitCode);
```

The output of the above example will be the standard output, standard error, and exit code of the `ls` command.

## Additional notes

* The `spawnCommand` function is a wrapper around the `spawn` function from the `child_process` module. For more information on the `spawn` function, please refer to the Node.js documentation.
* The `spawnCommand` function can be used to execute commands on both Windows and Linux systems.
* The `spawnCommand` function can be used to execute commands in a synchronous or asynchronous manner.
* The `spawnCommand` function can be used to capture the standard output, standard error, and exit code of a command.
  
  