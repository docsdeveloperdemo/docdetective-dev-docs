
  
   # **loadEnvsForObject**

## What does this do?

The `loadEnvsForObject` function takes an object as input and resolves all environment variables in the object's key-value pairs.

## Why should I use this?

This function is useful for loading environment variables into an object, which can be helpful for configuring applications or services.

## Prerequisites

There are no prerequisites for using this function.

## How to use this

To use this function, simply pass an object as the input parameter. The function will resolve all environment variables in the object's key-value pairs and return the updated object.

Here is an example of how to use the `loadEnvsForObject` function:

```javascript
const object = {
  "key1": "${ENV_VAR1}",
  "key2": "${ENV_VAR2}"
};

const updatedObject = loadEnvsForObject(object);

console.log(updatedObject);
// {
//   "key1": "value1",
//   "key2": "value2"
// }
```

## Additional notes

* The `loadEnvsForObject` function uses the `dotenv` library to resolve environment variables.
* The `dotenv` library must be installed in order to use the `loadEnvsForObject` function.
* The `loadEnvsForObject` function can be used to resolve environment variables in any type of object, not just JavaScript objects.
  
  