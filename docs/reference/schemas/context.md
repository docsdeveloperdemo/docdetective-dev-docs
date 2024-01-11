---
title: context
layout: default
nav_order: 1
parent: Reference
---




# context


## Description

An application and supported platforms.

If no contexts are specified but a context is required by one or more tests, Doc Detective attempts to identify a supported context in the current environment and run tests against it. For browsers, context priority is Firefox > Chrome > Chromium.

## Fields

Field | Type | Description | Default
:-- | :-- | :-- | :--
app | object |  Required. The application to run. | 
app.name | string |  Required. Name of the application.<br /><br />Accepted values: `firefox`, `chrome` | 
app.path | string |  Optional. Path to the application. If not specified, defaults to typical install paths per platform. If specified but the path is invalid, the context is skipped. | 
app.options | object |  Optional. Options to pass to the app. Only works when `name` is `firefox` or `chrome`. | 
app.options.width | integer |  Optional. Width of the window in pixels. | 
app.options.height | integer |  Optional. Height of the window in pixels. | 
app.options.headless | boolean |  Optional. If `true`, runs the browser in headless mode. | 
platforms | array of strings |  Required. Supported platforms for the application. | 

## Example

```json
{
  "app": {
    "name": "firefox"
  },
  "platforms": [
    "linux"
  ]
}
```

```json
{
  "app": {
    "name": "firefox",
    "options": {
      "width": 800,
      "height": 600,
      "headless": false
    }
  },
  "platforms": [
    "linux",
    "windows",
    "mac"
  ]
}
```

```json
{
  "app": {
    "name": "chrome"
  },
  "platforms": [
    "linux",
    "windows",
    "mac"
  ]
}
```

```json
{
  "app": {
    "name": "firefox",
    "path": "/usr/bin/firefox"
  },
  "platforms": [
    "linux"
  ]
}
```

