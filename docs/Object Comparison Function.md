
  
   # **httpRequest.js**

## What does this do?

The `httpRequest.js` file contains a function called `objectExistsInObject` that compares two objects and returns a status of "PASS" or "FAIL" along with a description of any differences found.

## Why should I use this?

The `objectExistsInObject` function can be used to test if a nested object exists within another object and if the values of the nested object match the expected values. This can be useful for testing the output of API calls or other functions that return complex objects.

## Prerequisites

There are no prerequisites for using the `objectExistsInObject` function.

## How to use this

To use the `objectExistsInObject` function, you must pass two objects as arguments: the expected object and the actual object. The function will then compare the two objects and return a status of "PASS" or "FAIL" along with a description of any differences found.

Here is an example of how to use the `objectExistsInObject` function:

```javascript
const expected = {
  name: "John Doe",
  age: 30,
  address: {
    street: "123 Main Street",
    city: "Anytown",
    state: "CA",
    zip: "12345",
  },
};

const actual = {
  name: "John Doe",
  age: 30,
  address: {
    street: "123 Main Street",
    city: "Anytown",
    state: "CA",
    zip: "12345",
  },
};

const result = objectExistsInObject(expected, actual);

console.log(result);
```

The output of the above code will be:

```
{
  status: "PASS",
  description: "",
}
```

This indicates that the two objects are identical and that there are no differences between them.

## Conclusion

The `objectExistsInObject` function is a useful tool for testing the output of API calls or other functions that return complex objects. It can help you to ensure that the data you are receiving is accurate and complete.
  
  