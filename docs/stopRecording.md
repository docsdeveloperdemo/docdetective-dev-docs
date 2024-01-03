
  
   # **stopRecording**

## What does this do?

The `stopRecording` method stops the recording of a video.

## Why should I use this?

You should use this method to stop recording a video after you have started it with the `startRecording` method.

## Prerequisites

Before you can use the `stopRecording` method, you must:

1.  Create a `WebDriver` instance.
2.  Start a recording session by calling the `startRecording` method.

## How to use this

To use the `stopRecording` method, call it with the following parameters:

* `config`: A `Config` object that contains the configuration for the recording session.
* `step`: A `Step` object that contains the information about the step that is being recorded.
* `driver`: A `WebDriver` instance.

The `stopRecording` method will return a `Result` object that contains the status of the recording session and a description of any errors that occurred.

## Example

The following code shows you how to use the `stopRecording` method:

```javascript
async function stopRecording(config, step, driver) {
  let result = {
    status: "PASS",
    description: "Started recording.",
  };

  // Validate step payload
  isValidStep = validate("stopRecording_v2", step);
  if (!isValidStep.valid) {
    result.status = "FAIL";
    result.description = `Invalid step definition: ${isValidStep.errors}`;
    return result;
  }

  // Set filePath
  if (!step.filePath) {
    step.filePath = path.join(config.mediaDirectory, `${step.id}.mp4`);
  }

  exit();
  try {
    // await driver.startRecording(step.filePath);
  } catch (error) {
    // Couldn't save screenshot
    result.status = "FAIL";
    result.description = `Couldn't save screenshot. ${error}`;
    return result;
  }

  // PASS
  return result;
}
```
  
  