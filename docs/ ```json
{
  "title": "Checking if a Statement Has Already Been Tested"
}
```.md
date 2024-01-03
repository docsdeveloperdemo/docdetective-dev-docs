
  
   #  ```json
{
  "title": "Checking if a Statement Has Already Been Tested"
}
```

## What does this do?
This method iterates through the list of tests in the spec and checks if any of them have an id that matches the id of the statementJson object. If a match is found, the idMatch variable is set to true.

## Why should I use this?
This method is used to determine if a statement has already been tested. If a statement has already been tested, it does not need to be tested again.

## Prerequisites
None.

## How to use this
To use this method, you must provide a spec object and a statementJson object. The spec object must contain a list of tests, and the statementJson object must contain an id property. The method will return true if a match is found, and false otherwise.

Here is an example of how to use this method:

```
const spec = {
  tests: [
    {
      id: '123',
      name: 'Test 1'
    },
    {
      id: '456',
      name: 'Test 2'
    }
  ]
};

const statementJson = {
  id: '123',
  name: 'Statement 1'
};

const idMatch = spec.tests.forEach((test) => {
  if (test.id && test.id === statementJson.id) idMatch = true;
});

console.log(idMatch); // true
```
  
  