
  
   # **buildRunShell**

## What does this do?

The `buildRunShell` function is used to construct the `runShell` action, which allows you to run a shell command on the target device.

## Why should I use this?

The `runShell` action can be used to execute any shell command on the target device, which can be useful for a variety of purposes, such as:

- Installing or updating software
- Configuring the device
- Troubleshooting issues

## Prerequisites

Before using the `runShell` action, you must first:

1. Enable USB debugging on the target device.
2. Install the Android Debug Bridge (ADB) on your computer.
3. Connect the target device to your computer using a USB cable.

## How to use this

To use the `runShell` action, simply call the `buildRunShell` function and pass in the following parameters:

- `config`: The configuration object for the `runShell` action.
- `match`: The match object for the `runShell` action.

The `config` object must contain the following properties:

- `device`: The target device.
- `adbPath`: The path to the ADB executable.

The `match` object must contain the following properties:

- `command`: The shell command to be executed.

Once you have called the `buildRunShell` function, the `runShell` action will be executed and the output of the shell command will be returned.

## Example

The following example shows how to use the `buildRunShell` function to run the `ls` command on the target device:

```javascript
const config = {
  device: device,
  adbPath: '/path/to/adb'
};

const match = {
  command: 'ls'
};

const action = buildRunShell(config, match);

action.run().then(output => {
  console.log(output);
});
```

## Additional notes

- The `runShell` action can be used to run any shell command, but it is important to note that some commands may require root access.
- If you are running a command that requires root access, you will need to add the `--root` flag to the `command` property of the `match` object.
- For example, the following command would run the `ls` command with root access:

```javascript
const match = {
  command: 'ls --root'
};
```
  
  