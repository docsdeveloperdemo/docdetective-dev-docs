
  
   # **goTo**

## What does this do?

The `goTo` method opens a URL in a new browser tab.

## Why should I use this?

Use the `goTo` method when you want to open a URL in a new browser tab from your application. This can be useful for opening links to external websites or resources, or for opening internal links to other pages in your application.

## Prerequisites

There are no prerequisites for using the `goTo` method.

## How to use this

To use the `goTo` method, you must provide a URL as the first argument. The URL can be any valid URL, including HTTP, HTTPS, and file URLs.

The following code sample shows you how to use the `goTo` method:

```javascript
// Import the DocDetective library
import DocDetective from 'doc-detective';

// Create a new DocDetective instance
const docDetective = new DocDetective();

// Open a URL in a new browser tab
docDetective.goTo('https://www.google.com');
```

## Additional information

The `goTo` method can also be used to open a URL in a new window or in the same window. To do this, you must specify the `target` option as the second argument. The `target` option can be one of the following values:

* `_blank`: Opens the URL in a new window
* `_self`: Opens the URL in the same window
* `_parent`: Opens the URL in the parent window
* `_top`: Opens the URL in the top window

The following code sample shows you how to open a URL in a new window:

```javascript
// Import the DocDetective library
import DocDetective from 'doc-detective';

// Create a new DocDetective instance
const docDetective = new DocDetective();

// Open a URL in a new window
docDetective.goTo('https://www.google.com', '_blank');
```
  
  