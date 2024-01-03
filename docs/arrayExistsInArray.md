
  
   # **arrayExistsInArray**

## What does this do?

The `arrayExistsInArray` function checks if an expected array is present in an actual array. It does this by iterating through the expected array and checking if each element is present in the actual array. If all elements are present, the function returns a status of "PASS". If any element is not present, the function returns a status of "FAIL" and a description of the missing element.

## Why should I use this?

The `arrayExistsInArray` function can be used to test if a set of expected values is present in an actual set of values. This can be useful for testing the output of a function or method, or for verifying that a data set is complete.

## Prerequisites

There are no prerequisites for using the `arrayExistsInArray` function.

## How to use this

To use the `arrayExistsInArray` function, you must provide two arguments:

* `expected`: The expected array.
* `actual`: The actual array.

The function will return a result object with the following properties:

* `status`: A string indicating the status of the comparison ("PASS" or "FAIL").
* `description`: A string describing the missing element (if any).

Here is an example of how to use the `arrayExistsInArray` function:

```javascript
const expected = [1, 2, 3];
const actual = [1, 2, 3, 4];

const result = arrayExistsInArray(expected, actual);

console.log(result);
// { status: 'PASS', description: '' }
```

In this example, the expected array is [1, 2, 3] and the actual array is [1, 2, 3, 4]. The `arrayExistsInArray` function will return a status of "PASS" because all of the elements in the expected array are present in the actual array.

Here is another example of how to use the `arrayExistsInArray` function:

```javascript
const expected = [1, 2, 3];
const actual = [1, 2];

const result = arrayExistsInArray(expected, actual);

console.log(result);
// { status: 'FAIL', description: 'Array '[3]' isn't present in expected array.' }
```

In this example, the expected array is [1, 2, 3] and the actual array is [1, 2]. The `arrayExistsInArray` function will return a status of "FAIL" because the element 3 is not present in the actual array.
  
  