
  
   # **httpRequest.js**

## What does this do?

The `httpRequest.js` file contains a function that checks if an object exists in another object. This function is used in the `doc-detective-core` library to check if a property exists in a configuration object.

## Why should I use this?

The `objectExistsInObject` function can be used to check if a property exists in a configuration object before using it. This can help to prevent errors from occurring if a property is not present.

## Prerequisites

There are no prerequisites for using the `objectExistsInObject` function.

## How to use this

To use the `objectExistsInObject` function, you must pass two objects as arguments. The first object is the object that you want to check for a property. The second object is the object that contains the property that you want to check for.

The `objectExistsInObject` function will return an object with the following properties:

* `result`: A string that indicates whether the property exists in the object. The possible values are "PASS" and "FAIL".
* `message`: A string that provides more information about the result.

Here is an example of how to use the `objectExistsInObject` function:

```javascript
const object1 = {
  name: "John Doe",
  age: 30
};

const object2 = {
  name: "Jane Doe"
};

const result = objectExistsInObject(object1, "age");

console.log(result);
```

The output of the above code will be:

```
{
  result: "PASS",
  message: "The property 'age' exists in the object."
}
```
  
  