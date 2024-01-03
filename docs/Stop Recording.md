
  
   # **stopRecording**

## What does this do?

The `stopRecording` method stops the currently active recording and saves the video to a file.

## Why should I use this?

You should use this method to stop recording a video after you have finished capturing the desired content.

## Prerequisites

Before you can use the `stopRecording` method, you must first start recording a video using the `startRecording` method.

## How to use this

To use the `stopRecording` method, call it with the following parameters:

* `videoDetails`: An object containing the following properties:
    * `recorder`: The recorder object that was created when you started recording.
    * `targetExtension`: The desired file extension for the saved video.
    * `height`: The desired height of the saved video in pixels.
    * `width`: The desired width of the saved video in pixels.
    * `filepath`: The desired path to the saved video file.
    * `tempFilepath`: The path to the temporary video file that was created during recording.
    * `fps`: The desired frame rate of the saved video in frames per second.
    * `targetFps`: The target frame rate of the saved video in frames per second.
* `config`: An object containing the following properties:
    * `browserOptions`: An object containing the browser options that were used to start recording.

The `stopRecording` method will return an object with the following properties:

* `status`: A string indicating the status of the recording. This can be either "PASS" or "FAIL".
* `description`: A string describing the result of the recording.

## Example

The following code shows you how to use the `stopRecording` method:

```javascript
async function stopRecording(videoDetails, config) {
  let status;
  let description;
  let result;

  if (typeof videoDetails.recorder === "undefined") {
    status = "PASS";
    description = `Skipping action. No action-defined recording in progress.`;
    result = { status, description };
    return { result };
  }

  recorder = videoDetails.recorder;
  targetExtension = videoDetails.targetExtension;
  height = videoDetails.height;
  width = videoDetails.width;
  filepath = videoDetails.filepath;
  tempFilepath = videoDetails.tempFilepath;
  fps = videoDetails.fps;
  targetFps = videoDetails.targetFps;

  try {
    await recorder.stop();
    if (
      targetExtension === ".gif" ||
      height != config.browserOptions.height ||
      width != config.browserOptions.width ||
      targetFps != fps
    ) {
      let output = await convertVideo(config, videoDetails);
      filepath = output;
    } else {
      fs.renameSync(tempFilepath, filepath);
      log(config, "debug", `Removed intermediate file: ${tempFilepath}`);
    }
    // PASS
    status = "PASS";
    description = `Stopped recording: ${filepath}`;
    result = { status, description };
    return { result };
  } catch {
    // FAIL: Couldn't capture screenshot
    status = "FAIL";
    description = `Couldn't stop recording.`;
    result = { status, description };
    return { result };
  }
}
```
  
  