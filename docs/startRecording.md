
  
   # **startRecording**

## What does this do?

The `startRecording` function starts recording a video of the browser window. The video is saved to a file in the specified directory.

## Why should I use this?

You can use this function to record videos of your web application for testing or demonstration purposes.

## Prerequisites

To use this function, you must have the following:

* A Puppeteer instance
* A web page to record

## How to use this

To use this function, call it with the following parameters:

* `action`: An object that contains the following properties:
    * `overwrite`: A boolean value that specifies whether to overwrite an existing file.
    * `mediaDirectory`: The directory where the video file will be saved.
    * `filename`: The name of the video file.
    * `fps`: The frame rate of the video.
    * `height`: The height of the video.
    * `width`: The width of the video.
* `page`: A Puppeteer page instance.
* `config`: A configuration object that contains the following properties:
    * `mediaDirectory`: The default directory where video files will be saved.
    * `browserOptions`: The options that will be used to launch the Puppeteer browser.

The function will return an object that contains the following properties:

* `result`: An object that contains the status of the recording and a description of the result.
* `videoDetails`: An object that contains the details of the video recording.

## Example

The following example shows how to use the `startRecording` function:

```javascript
async function startRecordingExample() {
  const puppeteer = require('puppeteer');
  const docDetective = require('doc-detective-core');

  const browser = await puppeteer.launch();
  const page = await browser.newPage();

  const config = {
    mediaDirectory: '/tmp/videos',
    browserOptions: {
      headless: false,
      width: 1280,
      height: 720,
    },
  };

  const action = {
    overwrite: false,
    mediaDirectory: '/tmp/videos',
    filename: 'my-video.mp4',
    fps: 30,
    height: 720,
    width: 1280,
  };

  const { result, videoDetails } = await docDetective.startRecording(action, page, config);

  console.log(result);
  console.log(videoDetails);

  await browser.close();
}

startRecordingExample();
```
  
  