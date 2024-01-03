
  
   # **Suggest**

## What does this do?

The `suggest` method is used to suggest a new markup for a given file type. It takes a file type and a markup name as arguments, and returns a new file type with the suggested markup added.

## Why should I use this?

The `suggest` method can be used to add new markups to file types that do not currently support them. This can be useful for adding support for new languages or file formats.

## Prerequisites

Before using the `suggest` method, you must first create a file type object. This can be done using the `createFileType` method.

## How to use this

To use the `suggest` method, simply call it with the file type and markup name as arguments. The following code shows how to suggest a new markup for the `json` file type:

```
const fileType = createFileType('json');
const markup = suggest(fileType, 'yaml');
```

The `markup` variable will now contain a new file type object with the `yaml` markup added.

## Example

The following code shows how to use the `suggest` method to add a new markup to the `json` file type:

```
const fileType = createFileType('json');
const markup = suggest(fileType, 'yaml');

console.log(markup.name); // 'json-yaml'
```

The output of the above code will be `json-yaml`, which is the name of the new file type with the `yaml` markup added.
  
  