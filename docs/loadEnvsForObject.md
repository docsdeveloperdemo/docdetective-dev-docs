
  
   # **loadEnvsForObject**

## What does this do?

The `loadEnvsForObject` function recursively resolves all environment variables in the values of an object. This is useful for loading configuration files or other data that may contain environment variables.

## Why should I use this?

Using the `loadEnvsForObject` function can help to ensure that your code is able to access environment variables regardless of how they are defined. This can be especially useful in cases where environment variables are defined in different ways on different platforms or environments.

## Prerequisites

There are no prerequisites for using the `loadEnvsForObject` function.

## How to use this

To use the `loadEnvsForObject` function, simply pass an object to the function and it will recursively resolve all environment variables in the values of the object. The following example shows how to use the `loadEnvsForObject` function:

```javascript
const object = {
  "key1": "${ENV_VAR1}",
  "key2": {
    "nestedKey1": "${ENV_VAR2}",
    "nestedKey2": "${ENV_VAR3}"
  }
};

const resolvedObject = loadEnvsForObject(object);

console.log(resolvedObject);
// {
//   "key1": "value1",
//   "key2": {
//     "nestedKey1": "value2",
//     "nestedKey2": "value3"
//   }
// }
```

In this example, the `loadEnvsForObject` function resolves the environment variables `ENV_VAR1`, `ENV_VAR2`, and `ENV_VAR3` in the values of the object. The resolved object is then logged to the console.

## Conclusion

The `loadEnvsForObject` function is a useful tool for resolving environment variables in the values of an object. This can be especially useful in cases where environment variables are defined in different ways on different platforms or environments.
  
  