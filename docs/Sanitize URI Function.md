
  
   # **sanitizeUri**

## What does this do?

The `sanitizeUri` function takes a URI (Uniform Resource Identifier) as input and returns a sanitized version of the URI.

## Why should I use this?

The `sanitizeUri` function is useful for ensuring that URIs are in a consistent format and that they are safe to use in applications. For example, the function can be used to add the "https://" protocol to URIs that do not have a protocol specified, and it can also be used to remove any whitespace from URIs.

## Prerequisites

There are no prerequisites for using the `sanitizeUri` function.

## How to use this

To use the `sanitizeUri` function, simply pass a URI as the input parameter. The function will return a sanitized version of the URI.

Here is an example of how to use the `sanitizeUri` function:

```javascript
const uri = "www.example.com";
const sanitizedUri = sanitizeUri(uri);
console.log(sanitizedUri); // Output: https://www.example.com
```

## Additional notes

The `sanitizeUri` function is a simple function that can be used to improve the consistency and safety of URIs. However, it is important to note that the function does not perform any validation on the URI. For example, the function does not check to see if the URI is a valid URL or if it points to a valid resource.
  
  