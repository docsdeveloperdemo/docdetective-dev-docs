
  
   # **httpRequest**

## What does this do?

The `httpRequest` action validates a URI.

## Why should I use this?

Use the `httpRequest` action to validate a URI.

## Prerequisites

None.

## How to use this

To use the `httpRequest` action, provide the following information:

- **URI**: The URI to validate.

```ts  
  // Prep
  defaults = {
    action: "httpRequest",
    uri: text,
  };
  action = {
    action: "httpRequest",
  };

  // URI (Required)
  // Define
  console.log("-");
  let message = constructPrompt("URI", defaults.uri);
  console.log("(Required) Which URI do you want to validate?");
  let uri = prompt(message);
  uri = uri || defaults.uri;
  // Required value. Return early if empty.
  if (!uri) {
    log(config, "warning", "Skipping markup. Required value is empty.");
    return null;
  }
  // Sanitize
  uri = sanitizeUri(uri);
  // Set
  action.uri = uri;
```
  
  