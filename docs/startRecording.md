
  
   # **startRecording**

## What does this do?

The `startRecording` method starts recording a video of the user's screen. The video is saved to the file path specified in the `step` object.

## Why should I use this?

You should use this method if you want to record a video of the user's screen for debugging purposes.

## Prerequisites

Before using this method, you must have the following prerequisites:

* An OBS WebSocket server running on your computer.
* The OBS WebSocket client library installed.

## How to use this

To use this method, you must first create a `step` object. The `step` object must contain the following properties:

* `id`: A unique identifier for the step.
* `filePath`: The file path to which the video should be saved.

Once you have created the `step` object, you can call the `startRecording` method. The `startRecording` method will return a `result` object. The `result` object will contain the following properties:

* `status`: The status of the recording.
* `description`: A description of the recording.

If the recording was successful, the `status` property will be set to "PASS". If the recording failed, the `status` property will be set to "FAIL". The `description` property will contain a description of the error that occurred.

## Example

The following code shows you how to use the `startRecording` method:

```javascript
async function startRecording(config, step, driver) {
  let result = {
    status: "PASS",
    description: "Started recording.",
  };

  // Validate step payload
  isValidStep = validate("startRecording_v2", step);
  if (!isValidStep.valid) {
    result.status = "FAIL";
    result.description = `Invalid step definition: ${isValidStep.errors}`;
    return result;
  }

  // Set filePath
  if (!step.filePath) {
    step.filePath = path.join(config.mediaDirectory, `${step.id}.mp4`);
  }

  try {
    // TODO: JS-based in-browser recording
    //   await driver.setTimeout({ script: 5000 })
    //   const execResult = await driver.execute((a, b, c, d) => {
    //     return 15
    // }, 1, 2, 3, 4)
    //   console.log(execResult);
    // TODO: OBS-based native app recording
    const obs = new OBSWebSocket();
    // TODO: Set password from config
    const { obsWebSocketVersion, negotiatedRpcVersion } = await obs.connect(
      "ws://127.0.0.1:4455",
      "doc-detective"
    );
    log(
      config,
      "debug",
      `Connected to server ${obsWebSocketVersion} (using RPC ${negotiatedRpcVersion})`
    );

    // TODO: Appium-based mobile recording
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
  
  