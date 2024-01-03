
  
   # **startRecording**

## What does this do?

The `startRecording` function is used to start recording a video of the current page. The video is saved to a file in the specified directory.

## Why should I use this?

You can use this function to record videos of your web pages for a variety of purposes, such as:

* Creating tutorials
* Demonstrating how to use a web application
* Capturing bugs and errors

## Prerequisites

To use this function, you must have the following:

* A Puppeteer instance
* A page object
* A configuration object

## How to use this

To use this function, simply call it with the following arguments:

* `action`: An object containing the following properties:
    * `overwrite`: A boolean value that specifies whether or not to overwrite an existing file.
    * `mediaDirectory`: The directory where the video file will be saved.
    * `filename`: The name of the video file.
    * `fps`: The frame rate of the video.
    * `height`: The height of the video.
    * `width`: The width of the video.
* `page`: A page object.
* `config`: A configuration object.

The function will return an object containing the following properties:

* `result`: An object containing the status of the recording and a description of the result.
* `videoDetails`: An object containing information about the video file.

## Example

The following example shows how to use the `startRecording` function to record a video of a web page:

```javascript
const puppeteer = require('puppeteer');

(async () => {
  const browser = await puppeteer.launch();
  const page = await browser.newPage();

  const config = {
    mediaDirectory: '/tmp',
    filename: 'my-video.mp4',
    fps: 30,
    height: 720,
    width: 1280
  };

  const action = {
    overwrite: false
  };

  const { result, videoDetails } = await startRecording(action, page, config);

  console.log(result);
  console.log(videoDetails);

  await browser.close();
})();
```
  
  