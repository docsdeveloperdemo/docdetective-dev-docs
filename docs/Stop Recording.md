
  
   # **stopRecording**

## What does this do?

The `stopRecording` method stops the current recording session and saves the recorded video to a file.

## Why should I use this?

Use this method to stop recording a video of the browser window. This can be useful for creating tutorials or demonstrations, or for capturing bugs and errors.

## Prerequisites

To use this method, you must first start a recording session using the `startRecording` method.

## How to use this

To use the `stopRecording` method, call it with the following parameters:

* `config`: A configuration object that specifies the directory where the video file should be saved.
* `step`: A step object that contains information about the recording session.
* `driver`: A WebDriver instance that represents the browser window that is being recorded.

The following code sample shows you how to use the `stopRecording` method:

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

## Example

The following code sample shows you how to use the `stopRecording` method to stop a recording session and save the recorded video to a file:

```javascript
const config = {
  mediaDirectory: "/path/to/media/directory",
};

const step = {
  id: "12345",
  filePath: "/path/to/video.mp4",
};

const driver = new WebDriver();

const result = await stopRecording(config, step, driver);

if (result.status === "PASS") {
  console.log("Recording saved successfully.");
} else {
  console.log("Error saving recording.");
}
```
  
  