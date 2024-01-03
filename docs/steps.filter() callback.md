
  
   # **validate**

## What does this do?

The `validate` function checks if a step is a valid step.

## Why should I use this?

You should use this function to ensure that the steps you are using are valid.

## Prerequisites

There are no prerequisites for using this function.

## How to use this

To use this function, you must pass in the name of the step and the step itself. The function will return a boolean value indicating whether or not the step is valid.

Here is an example of how to use this function:

```
const validation = validate('step_name', step);
if (!validation.valid) {
  log(
    config,
    'warning',
    `Step ${step} isn't a valid step. Skipping.`
  );
}
```

## Output

The `validate` function returns a boolean value indicating whether or not the step is valid.
  
  