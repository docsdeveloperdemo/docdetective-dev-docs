
  
   # **sanitizeUri**

## What does this do?

The `sanitizeUri` function takes a URI (Uniform Resource Identifier) as input and returns a sanitized version of the URI. The sanitization process involves the following steps:

1. Trimming any leading or trailing whitespace from the URI.
2. If the URI does not contain a protocol (e.g., "http://" or "https://"), the function adds the "https://" protocol to the beginning of the URI.

## Why should I use this?

The `sanitizeUri` function is useful for ensuring that URIs are in a consistent and valid format. This can be important for applications that need to process or interact with URIs, as it can help to prevent errors and ensure that URIs are handled correctly.

## Prerequisites

There are no prerequisites for using the `sanitizeUri` function.

## How to use this

To use the `sanitizeUri` function, simply pass the URI that you want to sanitize as the input parameter. The function will return the sanitized version of the URI.

Here is an example of how to use the `sanitizeUri` function:

```javascript
const uri = "www.example.com";
const sanitizedUri = sanitizeUri(uri);
console.log(sanitizedUri); // Output: https://www.example.com
```

## Conclusion

The `sanitizeUri` function is a simple but useful function that can help to ensure that URIs are in a consistent and valid format. This can be important for applications that need to process or interact with URIs, as it can help to prevent errors and ensure that URIs are handled correctly.
  
  