
  
   # **Suggest**

## What does this do?

The `suggest` method is used to suggest a new markup for a given file type. It takes a file type and a markup name as arguments, and returns a new file type with the suggested markup added.

## Why should I use this?

The `suggest` method can be used to add new markups to file types that do not currently support them. This can be useful for adding support for new languages or file formats.

## Prerequisites

Before using the `suggest` method, you must first create a file type object. This can be done using the `createFileType` method.

## How to use this

To use the `suggest` method, simply call it with the file type and markup name as arguments. The following example shows how to suggest a new markup for the `JavaScript` file type:

```
const fileType = createFileType('JavaScript');
const markup = suggest(fileType, 'markdown');
```

The `markup` variable will now contain a new file type object with the `markdown` markup added.

## Example

The following example shows how to use the `suggest` method to add support for the `markdown` markup to the `JavaScript` file type:

```
const fileType = createFileType('JavaScript');
const markup = suggest(fileType, 'markdown');

// Use the new file type to create a new document
const document = createDocument(markup, 'My Document');

// Save the document
saveDocument(document, 'my-document.md');
```

This will create a new markdown document with the title "My Document".
  
  