
  
   # **stopRecording**

## What does this do?

The `stopRecording` method stops the current recording and saves the video to a file.

## Why should I use this?

You should use this method to stop recording a video after you have finished capturing the desired content.

## Prerequisites

Before you can use the `stopRecording` method, you must first start recording a video using the `startRecording` method.

## How to use this

To use the `stopRecording` method, simply call the method on the `recorder` object. The method will take the following arguments:

* `videoDetails`: An object containing information about the video being recorded. This object must include the following properties:
    * `recorder`: The `recorder` object that is currently recording the video.
    * `targetExtension`: The desired file extension for the saved video.
    * `height`: The desired height of the saved video.
    * `width`: The desired width of the saved video.
    * `filepath`: The desired path to the saved video.
    * `tempFilepath`: The path to the temporary file that is being used to record the video.
    * `fps`: The desired frame rate of the saved video.
    * `targetFps`: The target frame rate of the saved video.
* `config`: An object containing configuration options for the `stopRecording` method. This object must include the following properties:
    * `browserOptions`: An object containing configuration options for the browser that is being used to record the video. This object must include the following properties:
        * `height`: The height of the browser window.
        * `width`: The width of the browser window.

The `stopRecording` method will return an object containing the following properties:

* `status`: The status of the recording. This property will be either "PASS" or "FAIL".
* `description`: A description of the recording status.

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
  
  