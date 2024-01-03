
  
   # **typeKeys**

## What does this do?

The `typeKeys` function types keys on the keyboard.

## Why should I use this?

This function can be used to type text into a text field, or to press keys on the keyboard to perform actions.

## Prerequisites

There are no prerequisites for using this function.

## How to use this

To use this function, you must provide the following parameters:

* `config`: The configuration object for the test.
* `step`: The step object for the test.
* `driver`: The driver object for the test.

The `config` object must contain the following properties:

* `specialKeyMap`: A map of special keys to their corresponding `Key` objects.

The `step` object must contain the following properties:

* `keys`: The keys to type.

The `driver` object must be a WebDriver object.

The following code sample shows you how to use the `typeKeys` function:

```javascript
async function typeKeys(config, step, driver) {
  // TODO: Add optional delay between keystrokes

  let result = { status: "PASS", description: "Typed keys." };

  // Validate step payload
  isValidStep = validate("typeKeys_v2", step);
  if (!isValidStep.valid) {
    result.status = "FAIL";
    result.description = `Invalid step definition: ${isValidStep.errors}`;
    return result;
  }

  // Convert string to array for consistency
  if (typeof step.keys === "string") step.keys = [step.keys];

  // Substitute special keys
  // 1. For each key, identify if it following the escape pattern of `$...$`.
  // 2. If it does, replace it with the corresponding `Key` object from `specialKeyMap`.
  step.keys = step.keys.map((key) => key.replace(/^\$.+\$$/gm, specialKeyMap[key]));

  // Run action
  try {
    await driver.keys(step.keys);
  } catch {
    // FAIL: Error opening URL
    result.status = "FAIL";
    result.description = "Couldn't type keys.";
    return result;
  }

  // PASS
  return result;
}
```
  
  