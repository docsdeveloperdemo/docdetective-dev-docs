
  
   # **arrayExistsInArray**

## What does this do?

The `arrayExistsInArray` function checks if an expected array is present in an actual array. It does this by iterating through the expected array and checking if each element is present in the actual array. If all elements are present, the function returns a status of "PASS". If any element is not present, the function returns a status of "FAIL" and a description of the missing element.

## Why should I use this?

The `arrayExistsInArray` function can be used to test if a particular array of values is present in another array. This can be useful for testing the output of a function or method that is expected to return an array of values.

## Prerequisites

There are no prerequisites for using the `arrayExistsInArray` function.

## How to use this

To use the `arrayExistsInArray` function, you simply pass in the expected array and the actual array as arguments. The function will then return a status of "PASS" or "FAIL" and a description of the missing element (if any).

Here is an example of how to use the `arrayExistsInArray` function:

```javascript
const expectedArray = [1, 2, 3];
const actualArray = [1, 2, 3, 4];

const result = arrayExistsInArray(expectedArray, actualArray);

console.log(result);
// { status: 'PASS', description: '' }
```

In this example, the expected array is [1, 2, 3] and the actual array is [1, 2, 3, 4]. The `arrayExistsInArray` function will return a status of "PASS" because all of the elements in the expected array are present in the actual array.

## Conclusion

The `arrayExistsInArray` function is a useful tool for testing if a particular array of values is present in another array. It is simple to use and can be used in a variety of situations.
  
  