
  
   # **moveMouse**

## What does this do?

The `moveMouse` function moves the mouse cursor to a specific location on the page, relative to an element. It can also be used to display the mouse cursor.

## Why should I use this?

The `moveMouse` function can be used to:

- Simulate user interactions with the page, such as clicking on buttons or links.
- Display the mouse cursor to help users understand what is happening on the page.
- Take screenshots of the page with the mouse cursor in a specific location.

## Prerequisites

The `moveMouse` function requires the following prerequisites:

- A Puppeteer page object.
- An element handle for the element that the mouse cursor should be moved to.
- An action object that specifies the alignment and offset of the mouse cursor.

## How to use this

To use the `moveMouse` function, you can follow these steps:

1. Create a Puppeteer page object.
2. Get an element handle for the element that the mouse cursor should be moved to.
3. Create an action object that specifies the alignment and offset of the mouse cursor.
4. Call the `moveMouse` function with the page object, element handle, and action object as arguments.

The following code sample shows how to use the `moveMouse` function:

```javascript
async function moveMouse(page, elementHandle, action) {
  // Set defaults
  const defaults = {
    alignH: "center",
    alignV: "center",
    offsetX: 0,
    offsetY: 0,
  };

  // Process fallbacks
  action.alignH = action.alignH || defaults.alignH;
  action.alignV = action.alignV || defaults.alignV;
  action.offsetX = action.offsetX || defaults.offsetX;
  action.offsetY = action.offsetY || defaults.offsetY;

  // Calc coordinates
  const bounds = await elementHandle.boundingBox();
  let x = bounds.x;
  if (action.offsetX) x = x + Number(action.offsetX);
  if (action.alignH) {
    let alignHOffset;
    if (action.alignH === "left") {
      alignHOffset = 10;
    } else if (action.alignH === "center") {
      alignHOffset = bounds.width / 2;
    } else if (action.alignH === "right") {
      alignHOffset = bounds.width - 10;
    } else {
      // FAIL
      return {
        status: "FAIL",
        description: `Invalid 'alignH' value.`,
      };
    }
    x = x + alignHOffset;
  }
  let y = bounds.y;
  if (action.offsetY) y = y + Number(action.offsetY);
  if (action.alignV) {
    let alignVOffset;
    if (action.alignV === "top") {
      alignVOffset = 10;
    } else if (action.alignV === "center") {
      alignVOffset = bounds.height / 2;
    } else if (action.alignV === "bottom") {
      alignVOffset = bounds.height - 10;
    } else {
      // FAIL
      return {
        status: "FAIL",
        description: `Invalid 'alignV' value.`,
      };
    }
    y = y + alignVOffset;
  }

  // Move
  await page.mouse.move(x, y, { steps: 25 });

  // Display mouse cursor
  await page.$eval("puppeteer-mouse-pointer", (e) => (e.style.display = "block"));

  // PASS
  return {
    status: "PASS",
    description: `Moved mouse to element.`,
  };
}
```

## Gotchas

There are a few things to keep in mind when using the `moveMouse` function:

- The `moveMouse` function is not guaranteed to work on all pages. Some pages may have restrictions on mouse movement, such as if the page is in a sandbox or if the user has disabled JavaScript.
- The `moveMouse` function may not work correctly if the element that the mouse cursor is being moved to is not visible on the page.
- The `moveMouse` function may not work correctly if the page is being rendered in a headless browser.
  
  