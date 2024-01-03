
  
   # **httpRequest**

## What does this do?

The `httpRequest` action validates a given URI.

## Why should I use this?

Use the `httpRequest` action to validate a URI before making a request. This can help to prevent errors and ensure that your requests are successful.

## Prerequisites

Before using the `httpRequest` action, you must have the following:

* A valid URI to validate.

## How to use this

To use the `httpRequest` action, follow these steps:

1.  In your code, import the `buildHttpRequest` function from the `doc-detective-core` library.
2.  Call the `buildHttpRequest` function with the following parameters:
    * `config`: The configuration object for the action.
    * `match`: The match object for the action.
3.  The `buildHttpRequest` function will return an action object.
4.  Add the action object to your action list.

The following code sample shows you how to use the `httpRequest` action:

```javascript
import { buildHttpRequest } from 'doc-detective-core';

const config = {
  // Configuration options for the action.
};

const match = {
  // Match object for the action.
};

const action = buildHttpRequest(config, match);

// Add the action object to your action list.
```

## Example

The following example shows you how to use the `httpRequest` action to validate a URI:

```javascript
import { buildHttpRequest } from 'doc-detective-core';

const config = {
  // Configuration options for the action.
};

const match = {
  // Match object for the action.
};

const action = buildHttpRequest(config, match);

if (action) {
  // The URI is valid.
} else {
  // The URI is not valid.
}
```
  
  