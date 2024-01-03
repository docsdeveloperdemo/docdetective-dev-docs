
  
   # **buildFind**

## What does this do?

The `buildFind` function is used to construct an action object that can be used to find an element on a page and perform various actions on it.

## Why should I use this?

The `buildFind` function is useful for automating tasks that require interacting with specific elements on a page. For example, you could use it to click a button, type text into an input field, or move the mouse to a specific location.

## Prerequisites

Before using the `buildFind` function, you must first install the `doc-detective-core` package. You can do this by running the following command in your terminal:

```
npm install doc-detective-core
```

## How to use this

To use the `buildFind` function, you must first create a configuration object. This object should contain the following properties:

* `action`: The action that you want to perform on the element. This can be one of the following values:
    * `find`
    * `click`
    * `type`
    * `moveMouse`
* `css`: The CSS selector for the element that you want to find.
* `matchText`: The text that you expect the element to have.
* `moveMouse`: A boolean value that indicates whether or not you want to move the mouse to the element.
* `click`: A boolean value that indicates whether or not you want to click the element.
* `type`: A string that contains the text that you want to type into the element.
* `specialTrailingKey`: A string that contains the special key that you want to press after typing the text.

Once you have created the configuration object, you can call the `buildFind` function and pass it the configuration object as an argument. The function will return an action object that you can use to perform the desired action on the element.

Here is an example of how to use the `buildFind` function:

```
const config = {
  action: "find",
  css: ".btn-primary",
  matchText: "Click me",
  moveMouse: true,
  click: true,
  type: null,
  specialTrailingKey: null
};

const action = buildFind(config);

// Use the action object to perform the desired action on the element
```

## Relevant method or class

The `buildFind` function uses the following methods and classes:

* `prompt`: The `prompt` function is used to get input from the user.
* `log`: The `log` function is used to log messages to the console.
* `constructPrompt`: The `constructPrompt` function is used to construct a message that is displayed to the user.

## Conclusion

The `buildFind` function is a powerful tool that can be used to automate tasks that require interacting with specific elements on a page. By following the instructions in this document, you can learn how to use the `buildFind` function to its full potential.
  
  