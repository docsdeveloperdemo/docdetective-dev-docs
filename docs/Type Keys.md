
  
   # **typeKeys**

## What does this do?

The `typeKeys` method types keys into the active element.

## Why should I use this?

Use this method to simulate user input by typing keys into the active element. This can be useful for testing forms, text inputs, and other interactive elements.

## Prerequisites

Before using the `typeKeys` method, you must first:

1.  Install the `doc-detective-core` package.
2.  Import the `typeKeys` method into your test file.

```javascript
import { typeKeys } from 'doc-detective-core';
```

## How to use this

To use the `typeKeys` method, simply call it with the following parameters:

* `config`: A configuration object that contains the following properties:
    * `driver`: A WebDriver instance.
    * `step`: A step object that contains the following properties:
        * `keys`: An array of keys to type.
        * `delay`: An optional delay (in milliseconds) between keystrokes.
* `driver`: A WebDriver instance.
* `step`: A step object that contains the following properties:
    * `keys`: An array of keys to type.
    * `delay`: An optional delay (in milliseconds) between keystrokes.

The following code sample shows you how to use the `typeKeys` method to type the word "Hello" into a text input:

```javascript
const config = {
  driver: driver,
  step: {
    keys: ['H', 'e', 'l', 'l', 'o'],
  },
};

typeKeys(config, step, driver);
```

## Example

The following code sample shows you how to use the `typeKeys` method to type the word "Hello" into a text input:

```javascript
const config = {
  driver: driver,
  step: {
    keys: ['H', 'e', 'l', 'l', 'o'],
  },
};

typeKeys(config, step, driver);
```
  
  