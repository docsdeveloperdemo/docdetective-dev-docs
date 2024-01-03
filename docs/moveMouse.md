
  
   # **moveMouse**

## What does this do?

The `moveMouse` function moves the mouse cursor to a specific position on the page, relative to a given element. It also displays the mouse cursor on the page.

## Why should I use this?

The `moveMouse` function can be used to simulate user interactions with the page, such as clicking on buttons or selecting text. It can also be used to draw attention to a specific element on the page.

## Prerequisites

To use the `moveMouse` function, you must have a Puppeteer page object. You can create a page object by calling the `browser.newPage()` method.

## How to use this

To use the `moveMouse` function, call it with the following parameters:

* `action`: An object that specifies the position and alignment of the mouse cursor. The `action` object can have the following properties:
    * `alignH`: The horizontal alignment of the mouse cursor. Can be one of `"left"`, `"center"`, or `"right"`.
    * `alignV`: The vertical alignment of the mouse cursor. Can be one of `"top"`, `"center"`, or `"bottom"`.
    * `offsetX`: The horizontal offset of the mouse cursor, in pixels.
    * `offsetY`: The vertical offset of the mouse cursor, in pixels.
* `page`: The Puppeteer page object.
* `elementHandle`: The Puppeteer element handle of the element that the mouse cursor should be moved to.
* `config`: An object that specifies the configuration options for the `moveMouse` function. The `config` object can have the following properties:
    * `videoDetails`: An object that specifies the video recording details.
    * `debugRecording`: An object that specifies the debug recording details.

The `moveMouse` function will return an object with the following properties:

* `status`: The status of the mouse move operation. Can be one of `"PASS"` or `"FAIL"`.
* `description`: A description of the mouse move operation.

## Example

The following example shows how to use the `moveMouse` function to move the mouse cursor to the center of a button element:

```javascript
const puppeteer = require('puppeteer');

(async () => {
  const browser = await puppeteer.launch();
  const page = await browser.newPage();
  await page.goto('https://example.com');

  const buttonElement = await page.$('button');
  const bounds = await buttonElement.boundingBox();
  const x = bounds.x + bounds.width / 2;
  const y = bounds.y + bounds.height / 2;

  await page.mouse.move(x, y);

  await browser.close();
})();
```
  
  