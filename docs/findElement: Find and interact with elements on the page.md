
  
   # **findElement**

## What does this do?

The `findElement` function is used to find an element on the page and perform various actions on it, such as clicking, typing, and moving the mouse.

## Why should I use this?

The `findElement` function is a convenient way to interact with elements on the page without having to write a lot of code. It can also be used to automate tasks that would otherwise be difficult or time-consuming to do manually.

## Prerequisites

Before using the `findElement` function, you must first import the `webdriverio` library. You can do this by adding the following line to your code:

```
const webdriverio = require('webdriverio');
```

## How to use this

To use the `findElement` function, you must first create a `webdriverio` client. You can do this by calling the `webdriverio.remote()` function. The following code shows how to create a client for the Chrome browser:

```
const client = webdriverio.remote({
  desiredCapabilities: {
    browserName: 'chrome'
  }
});
```

Once you have created a client, you can use the `findElement` function to find an element on the page. The following code shows how to find an element by its CSS selector:

```
const element = await client.$('selector');
```

Once you have found an element, you can perform various actions on it. The following code shows how to click an element:

```
await element.click();
```

The `findElement` function can also be used to find multiple elements on the page. The following code shows how to find all elements with the class name "button":

```
const elements = await client.$$('.button');
```

The `findElement` function is a powerful tool that can be used to automate a wide variety of tasks. For more information, please see the [webdriverio documentation](https://webdriver.io/docs/api/element/).
  
  