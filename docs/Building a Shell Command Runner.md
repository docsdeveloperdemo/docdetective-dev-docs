
  
   # **buildRunShell**

## What does this do?

The `buildRunShell` function constructs an action object for running a shell command. It prompts the user for the command to run and splits the command into the command itself and its arguments.

## Why should I use this?

The `buildRunShell` function is useful for running shell commands from within a Node.js script. It provides a simple way to prompt the user for the command to run and to handle the splitting of the command into the command itself and its arguments.

## Prerequisites

To use the `buildRunShell` function, you must have Node.js installed.

## How to use this

To use the `buildRunShell` function, import it into your Node.js script and call it with the following arguments:

* `config`: A configuration object that contains the following properties:
    * `cwd`: The current working directory.
    * `env`: The environment variables to use when running the command.
* `match`: A regular expression that matches the lines of code that you want to document.

The `buildRunShell` function will return an action object that can be used to run the shell command.

## Example

The following example shows how to use the `buildRunShell` function to run a shell command:

```javascript
const docDetective = require('doc-detective');

const config = {
  cwd: '/Users/andrewvanbeek/dev-docs-work/clients/doc-detective-core',
  env: {
    PATH: '/usr/local/bin:/usr/bin:/bin:/usr/sbin:/sbin'
  }
};

const match = /function buildRunShell\(config, match\) {/;

const action = docDetective.buildRunShell(config, match);

console.log(action);
```

The output of the above example will be:

```json
{
  "action": "runShell",
  "command": "ls",
  "args": []
}
```
  
  