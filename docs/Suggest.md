
  
   # **Suggest**

## What does this do?

The `suggest` method returns a list of suggested actions for the user. These actions can be used to help the user complete their task more quickly and easily.

## Why should I use this?

The `suggest` method can be used to improve the user experience by providing them with helpful suggestions. This can help to reduce the amount of time that the user spends searching for the information that they need.

## Prerequisites

There are no prerequisites for using the `suggest` method.

## How to use this

To use the `suggest` method, you must first create a `Suggest` object. You can then use the `suggest` method to return a list of suggested actions.

The following code sample shows you how to use the `suggest` method:

```
const suggest = new Suggest();

const actions = suggest.suggest();

actions.forEach((action) => {
  console.log(action);
});
```

The output of the code sample will be a list of suggested actions. Each action will be represented by a string.

## Example

The following code sample shows you how to use the `suggest` method to provide suggestions for a user who is searching for a product.

```
const suggest = new Suggest();

const actions = suggest.suggest('product');

actions.forEach((action) => {
  console.log(action);
});
```

The output of the code sample will be a list of suggested products. Each product will be represented by a string.
  
  