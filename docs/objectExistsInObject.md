
  
   # **httpRequest.js**

## What does this do?

The `httpRequest.js` file contains a function called `objectExistsInObject` that compares two objects and returns a status of "PASS" or "FAIL" and a description of any differences found.

## Why should I use this?

This function can be used to test if a nested object contains all of the keys and values of another object. This can be useful for testing the output of a function or method that returns an object, or for comparing two objects to see if they are equal.

## Prerequisites

There are no prerequisites for using this function.

## How to use this

To use the `objectExistsInObject` function, you must pass two objects as arguments: the expected object and the actual object. The function will then compare the two objects and return a status of "PASS" or "FAIL" and a description of any differences found.

Here is an example of how to use the `objectExistsInObject` function:

```javascript
const expected = {
  name: 'John Doe',
  age: 30,
  address: {
    street: '123 Main Street',
    city: 'Anytown',
    state: 'CA',
    zip: '12345'
  }
};

const actual = {
  name: 'John Doe',
  age: 30,
  address: {
    street: '123 Main Street',
    city: 'Anytown',
    state: 'CA',
    zip: '12345'
  }
};

const result = objectExistsInObject(expected, actual);

console.log(result);
```

The output of the above code will be:

```
{
  status: 'PASS',
  description: ''
}
```

This indicates that the two objects are equal.

## Conclusion

The `objectExistsInObject` function is a useful tool for testing if a nested object contains all of the keys and values of another object. This can be useful for testing the output of a function or method that returns an object, or for comparing two objects to see if they are equal.
  
  