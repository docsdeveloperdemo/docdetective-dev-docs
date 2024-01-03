
  
   # **Record**

## What does this do?

The `record` function executes a command and returns the standard output, standard error, and exit code.

## Why should I use this?

The `record` function can be used to execute commands and capture the output for later use. This can be useful for debugging purposes or for automating tasks.

## Prerequisites

The `record` function requires the following prerequisites:

* Node.js 8.0 or later
* The `fs` module
* The `child_process` module

## How to use this

To use the `record` function, simply pass the command you want to execute as the first argument. The function will then execute the command and return an object containing the standard output, standard error, and exit code.

Here is an example of how to use the `record` function:

```javascript
const { record } = require('doc-detective-core');

const command = 'ls -l';

record(command, (error, stdout, stderr) => {
  if (error) {
    console.error(error.message);
    return;
  }

  console.log(stdout);
  console.error(stderr);
});
```

## Output

The `record` function will return an object containing the following properties:

* `stdout`: The standard output of the command.
* `stderr`: The standard error of the command.
* `exitCode`: The exit code of the command.

## Example

The following example shows how to use the `record` function to execute the `ls -l` command and capture the output:

```javascript
const { record } = require('doc-detective-core');

const command = 'ls -l';

record(command, (error, stdout, stderr) => {
  if (error) {
    console.error(error.message);
    return;
  }

  console.log(stdout);
  console.error(stderr);
});
```

Output:

```
total 12
drwxr-xr-x  3 andrewvanbeek  staff   96 Aug 24 11:38 Applications
drwxr-xr-x  3 andrewvanbeek  staff   96 Aug 24 11:38 Desktop
drwxr-xr-x  3 andrewvanbeek  staff   96 Aug 24 11:38 Documents
drwxr-xr-x  3 andrewvanbeek  staff   96 Aug 24 11:38 Downloads
drwxr-xr-x  3 andrewvanbeek  staff   96 Aug 24 11:38 Library
drwxr-xr-x  3 andrewvanbeek  staff   96 Aug 24 11:38 Movies
drwxr-xr-x  3 andrewvanbeek  staff   96 Aug 24 11:38 Music
drwxr-xr-x  3 andrewvanbeek  staff   96 Aug 24 11:38 Pictures
drwxr-xr-x  3 andrewvanbeek  staff   96 Aug 24 11:38 Public
drwxr-xr-x  3 andrewvanbeek  staff   96 Aug 24 11:38 Sites
```
  
  