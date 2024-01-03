
  
   # Checking if a Test ID Exists

## What does this do?
This method checks if a test ID exists in the list of tests.

## Why should I use this?
This method can be used to determine if a test has already been executed.

## Prerequisites
None.

## How to use this
To use this method, pass the test ID as the first argument. The method will return a boolean value indicating whether or not the test ID exists in the list of tests.

Here is an example of how to use this method:

```
const testId = '12345';
const idMatch = spec.tests.some((test) => test.id === testId);

if (idMatch) {
  // The test has already been executed.
} else {
  // The test has not been executed yet.
}
```
  
  