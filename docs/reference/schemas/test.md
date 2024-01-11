 ---
title: test
layout: default
nav_order: 1
parent: Reference
---

# test

## Description

A Doc Detective test.

## Fields

| Field         | Type                                           | Description                                                                                                                   | Default         |
|---------------|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|-----------------|
| `id`          | `string`                                       | Optional. Unique identifier for the test.                                                                                     | Generated UUID  |
| `description` | `string`                                       | Optional. Description of the test.                                                                                            |                 |
| `file`        | `string`                                       | Optional. Path to the file that the test is associated with.                                                                  |                 |
| `detectSteps` | `boolean`                                      | Optional. Whether or not to detect steps in input files based on markup regex. Defaults to `true`.                            |                 |
| `contexts`    | array of object([context](/reference/schemas/context)) | Optional. Application/platform sets to run the test in. Overrides `contexts` defined at the config-level and spec-level.      |                 |
| `setup`       | `string`                                       | Optional. Path to a test specification to perform before this test, while maintaining this test's context.                    |                 |
| `cleanup`     | `string`                                       | Optional. Path to a test specification to perform after this test, while maintaining this test's context.                     |                 |
| `steps`       | array of objects                               | Required. Actions to perform as part of the test. Performed in the sequence defined. If one or more actions fail, the test fails. |                 |

The `steps` field can include an array of various objects like `checkLink`, `goTo`, `httpRequest`, `runShell`, `saveScreenshot`, `setVariables`, `typeKeys`, `find`, and `wait`.

## Examples

```json
{
  "steps": [
    {
      "action": "checkLink",
      "url": "https://www.duckduckgo.com"
    }
  ]
}
```

```json
{
  "steps": [
    {
      "action": "goTo",
      "url": "https://www.duckduckgo.com"
    },
    {
      "action": "find",
      "selector": "[title=Search]",
      "click": true,
      "typeKeys": {
        "keys": [
          "shorthair cats",
          "$ENTER$"
        ]
      }
    }
  ]
}
```

```json
{
  "id": "Do all the things! - Test",
  "description": "This test includes every property across all actions.",
  "contexts": [
    {
      "app": {
        "name": "firefox",
        "path": "/usr/bin/firefox"
      },
      "platforms": [
        "linux"
      ]
    }
  ],
  "setup": "setup.json",
  "cleanup": "cleanup.json",
  "steps": [
    {
      "action": "setVariables",
      "path": ".env"
    },
    {
      "action": "runShell",
      "command": "echo",
      "args": [
        "$USER"
      ]
    },
    {
      "action": "checkLink",
      "url": "https://www.duckduckgo.com"
    },
    {
      "action": "httpRequest",
      "url": "https://reqres.in/api/users",
      "method": "post",
      "requestData": {
        "name": "morpheus",
        "job": "leader"
      },
      "responseData": {
        "name": "morpheus",
        "job": "leader"
      },
      "statusCodes": [
        200,
        201
      ]
    },
    {
      "action": "goTo",
      "url": "https://www.duckduckgo.com"
    },
    {
      "action": "find",
      "selector": "[title=Search]",
      "timeout": 10000,
      "matchText": "Search",
      "moveTo": true,
      "click": true,
      "typeKeys": {
        "keys": [
          "shorthair cat"
        ]
      }
    },
    {
      "action": "typeKeys",
      "keys": [
        "$ENTER$"
      ]
    },
    {
      "action": "saveScreenshot"
    }
  ]
}
```
