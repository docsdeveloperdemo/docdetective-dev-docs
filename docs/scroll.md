
  
   # **scroll**

## What does this do?

The `scroll` function scrolls the page according to the specified action.

## Why should I use this?

This function is useful for testing the scrolling functionality of a web page. It can be used to verify that the page scrolls smoothly and that the correct content is displayed after scrolling.

## Prerequisites

Before using the `scroll` function, you must first import the `doc-detective-core` module. You can do this by adding the following line to your code:

```javascript
import { scroll } from 'doc-detective-core';
```

## How to use this

To use the `scroll` function, you must provide the following arguments:

* `action`: An object that specifies the x and y coordinates of the scroll action.
* `page`: A Puppeteer page object.
* `config`: An object that contains the configuration options for the scroll action.

The following code sample shows how to use the `scroll` function:

```javascript
const action = {
  x: 100,
  y: 200
};

const page = await browser.newPage();

const config = {
  videoDetails: {},
  debugRecording: {}
};

const result = await scroll(action, page, config);

console.log(result);
```

The output of the above code sample will be an object that contains the status and description of the scroll action.

## Output

The `scroll` function returns an object that contains the following properties:

* `status`: A string that indicates the status of the scroll action. The possible values are "PASS" and "FAIL".
* `description`: A string that describes the scroll action.
  
  