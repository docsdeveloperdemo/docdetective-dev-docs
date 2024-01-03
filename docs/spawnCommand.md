
  
   # **spawnCommand**

## What does this do?

The `spawnCommand` function executes a command in the operating system's shell and returns the standard output, standard error, and exit code of the command.

## Why should I use this?

The `spawnCommand` function is useful for running commands that are not built into Node.js or for running commands that require access to the operating system's shell.

## Prerequisites

There are no prerequisites for using the `spawnCommand` function.

## How to use this

To use the `spawnCommand` function, you must provide the following arguments:

* `cmd`: The command to execute.
* `args`: An array of arguments to pass to the command.
* `options`: An object of options to configure the behavior of the command.

The following example shows how to use the `spawnCommand` function to execute the `ls` command:

```javascript
const { spawnCommand } = require('doc-detective-core');

const { stdout, stderr, exitCode } = await spawnCommand('ls', ['-l']);

console.log(stdout);
console.log(stderr);
console.log(exitCode);
```

## Output

The `spawnCommand` function returns an object with the following properties:

* `stdout`: The standard output of the command.
* `stderr`: The standard error of the command.
* `exitCode`: The exit code of the command.

## Example

The following example shows how to use the `spawnCommand` function to execute the `ls` command and capture the standard output, standard error, and exit code of the command:

```javascript
const { spawnCommand } = require('doc-detective-core');

const { stdout, stderr, exitCode } = await spawnCommand('ls', ['-l']);

console.log(stdout);
console.log(stderr);
console.log(exitCode);
```

## Output

The output of the above example will be similar to the following:

```
total 16
drwxr-xr-x  3 andrewvanbeek  staff  102 Oct 25 12:38 Applications
drwxr-xr-x  4 andrewvanbeek  staff  136 Oct 25 12:38 Desktop
drwxr-xr-x  4 andrewvanbeek  staff  136 Oct 25 12:38 Documents
drwxr-xr-x  3 andrewvanbeek  staff  102 Oct 25 12:38 Downloads
drwxr-xr-x  3 andrewvanbeek  staff  102 Oct 25 12:38 Library
drwxr-xr-x  3 andrewvanbeek  staff  102 Oct 25 12:38 Movies
drwxr-xr-x  3 andrewvanbeek  staff  102 Oct 25 12:38 Music
drwxr-xr-x  3 andrewvanbeek  staff  102 Oct 25 12:38 Pictures
drwxr-xr-x  3 andrewvanbeek  staff  102 Oct 25 12:38 Public
drwxr-xr-x  3 andrewvanbeek  staff  102 Oct 25 12:38 Sites
```
  
  