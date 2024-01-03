
  
   # **goTo**

## What does this do?

The `goTo` method opens a URL in a new browser tab.

## Why should I use this?

The `goTo` method is useful for opening links from within your application. For example, you could use the `goTo` method to open a user's profile page when they click on their name.

## Prerequisites

There are no prerequisites for using the `goTo` method.

## How to use this

To use the `goTo` method, you must provide a URL. The URL can be a string or a `URL` object.

```ts  
// Open a URL in a new browser tab
goTo("https://www.google.com");

// Open a URL in a new browser tab with a custom title
goTo("https://www.google.com", "Google");
```

## Additional information

The `goTo` method can also be used to open a URL in a new window. To do this, you must set the `target` property of the `goTo` method to `"_blank"`.

```ts  
// Open a URL in a new window
goTo("https://www.google.com", "_blank");
```

The `goTo` method can also be used to open a URL in a new tab in the background. To do this, you must set the `background` property of the `goTo` method to `true`.

```ts  
// Open a URL in a new tab in the background
goTo("https://www.google.com", "_blank", true);
```
  
  