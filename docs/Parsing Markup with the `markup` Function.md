
  
   # Parsing Markup with the `markup` Function

## What does this do?

The `markup` function in the `utils.js` file is used to parse a line of text and identify any markup that is present. Markup is a special type of text that is used to format or annotate text, such as bold, italic, or strikethrough. The `markup` function uses a regular expression to match the markup in the line of text, and then it takes an action based on the type of markup that is found.

## Why should I use this?

The `markup` function is useful for parsing text that contains markup and taking action based on the type of markup that is found. This can be used to format text, extract data from text, or perform other tasks.

## Prerequisites

There are no prerequisites for using the `markup` function.

## How to use this

To use the `markup` function, you first need to import it into your code. You can do this by adding the following line to your code:

```javascript
import { markup } from 'doc-detective-core';
```

Once you have imported the `markup` function, you can use it to parse a line of text and identify any markup that is present. The following code shows how to use the `markup` function to parse a line of text and identify any bold markup:

```javascript
const line = 'This is a **bold** line of text.';
const markup = markup(line);
const boldMarkup = markup.filter(m => m.name === 'bold');
```

The `boldMarkup` variable will now contain an array of objects that represent the bold markup in the line of text. Each object will contain the following properties:

* `name`: The name of the markup type.
* `regex`: The regular expression that was used to match the markup.
* `actions`: An array of actions that should be taken based on the markup.

In the case of the bold markup, the `actions` array will contain a single object with the following properties:

* `name`: The name of the action.
* `params`: An object containing the parameters for the action.

In the case of the bold markup, the `params` object will contain the following property:

* `selector`: The CSS selector that should be used to select the bold text.

You can use the `markup` function to take any action that you want based on the type of markup that is found. For example, you could use the `markup` function to format text, extract data from text, or perform other tasks.
  
  