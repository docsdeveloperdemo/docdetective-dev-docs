
  
   # **convertVideo**

## What does this do?

The `convertVideo` function converts a video file to a specified format and resolution. It uses the `ffmpeg` command-line tool to perform the conversion.

## Why should I use this?

You should use this function if you need to convert a video file to a different format or resolution. For example, you might need to convert a video file to MP4 format for playback on a mobile device, or you might need to convert a video file to a lower resolution for streaming over the internet.

## Prerequisites

Before you can use the `convertVideo` function, you must have the `ffmpeg` command-line tool installed on your system. You can download `ffmpeg` from the [ffmpeg website](https://ffmpeg.org/).

## How to use this

To use the `convertVideo` function, you must provide the following arguments:

* `config`: A configuration object that contains the following properties:
    * `browserOptions`: An object that contains the following properties:
        * `height`: The height of the browser window in pixels.
        * `width`: The width of the browser window in pixels.
* `videoDetails`: An object that contains the following properties:
    * `tempFilepath`: The path to the temporary video file.
    * `filepath`: The path to the output video file.
    * `fps`: The frame rate of the video in frames per second.
    * `targetExtension`: The target file extension of the video file.
    * `height`: The height of the video in pixels.
    * `width`: The width of the video in pixels.

The `convertVideo` function will return an object that contains the following properties:

* `stdout`: The standard output from the `ffmpeg` command.
* `stderr`: The standard error from the `ffmpeg` command.
* `error`: An error message if the conversion failed.

## Example

The following example shows how to use the `convertVideo` function to convert a video file to MP4 format:

```javascript
const convertVideo = require("./record");

const config = {
  browserOptions: {
    height: 1080,
    width: 1920
  }
};

const videoDetails = {
  tempFilepath: "/path/to/temp/video.mp4",
  filepath: "/path/to/output/video.mp4",
  fps: 30,
  targetExtension: ".mp4",
  height: 1080,
  width: 1920
};

const result = convertVideo(config, videoDetails);

if (result.error) {
  console.error(result.error);
} else {
  console.log(result.stdout);
}
```
  
  