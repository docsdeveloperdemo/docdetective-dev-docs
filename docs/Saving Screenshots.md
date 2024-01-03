
  
   # **saveScreenshot**

## What does this do?

The `saveScreenshot` method saves a screenshot of the current browser window to a file.

## Why should I use this?

You can use the `saveScreenshot` method to capture a visual representation of the current state of the browser window. This can be useful for debugging purposes, or for creating documentation or tutorials.

## Prerequisites

To use the `saveScreenshot` method, you must have the following:

* A web browser that supports the `saveScreenshot` method.
* A file system location where you want to save the screenshot.

## How to use this

To use the `saveScreenshot` method, follow these steps:

1. Open the web browser that you want to use.
2. Navigate to the web page that you want to capture.
3. Call the `saveScreenshot` method.
4. Specify the file system location where you want to save the screenshot.
5. The screenshot will be saved to the specified file system location.

## Example

The following code shows you how to use the `saveScreenshot` method:

```javascript
async function saveScreenshot(config, step, driver) {
  let result = {
    status: "PASS",
    description: "Saved screenshot.",
  };

  // Validate step payload
  isValidStep = validate("saveScreenshot_v2", step);
  if (!isValidStep.valid) {
    result.status = "FAIL";
    result.description = `Invalid step definition: ${isValidStep.errors}`;
    return result;
  }

  // Set file name
  step.path = step.path || `${step.id}.png`;

  // Set path directory
  const dir =
    step.directory ||
    config.runTests?.mediaDirectory ||
    config.runTests?.output ||
    config.output;
  // If `dir` doesn't exist, create it
  if (!fs.existsSync(dir)) {
    fs.mkdirSync(dir, { recursive: true });
  }
  // Set filePath
  filePath = path.join(dir, step.path);

  // Check if file already exists
  let existFilePath;
  if (fs.existsSync(filePath)) {
    if (step.overwrite == "false") {
      // File already exists
      result.status = "SKIP";
      result.description = `File already exists: ${filePath}`;
      return result;
    } else {
      // Set temp file path
      existFilePath = filePath;
      filePath = path.join(dir, `${step.id}_${Date.now()}.png`);
    }
  }

  try {
    await driver.saveScreenshot(filePath);
  } catch (error) {
    // Couldn't save screenshot
    result.status = "FAIL";
    result.description = `Couldn't save screenshot. ${error}`;
    return result;
  }

  // If file already exists
  // If overwrite is true, replace old file with new file
  // If overwrite is byVariance, compare files and replace if variance is greater than threshold
  if (existFilePath) {
    let percentDiff;

    // Perform numerical pixel diff with pixelmatch
    if (step.maxVariation) {
      const img1 = PNG.sync.read(fs.readFileSync(existFilePath));
      const img2 = PNG.sync.read(fs.readFileSync(filePath));

      // Compare wight and height of images
      if (img1.height !== img2.height || img1.width !== img2.width) {
        result.status = "FAIL";
        result.description = `Couldn't compare images. Images are not the same size.`;
        return result;
      }

      const { width, height } = img1;
      const numDiffPixels = pixelmatch(
        img1.data,
        img2.data,
        null,
        width,
        height,
        { threshold: 0.005 }
      );
      percentDiff = (numDiffPixels / (width * height)) * 100;

      log(config, "debug", {totalPixels: width * height, numDiffPixels, percentDiff})

      if (percentDiff > step.maxVariation) {
        if (step.overwrite == "byVariation") {
          // Replace old file with new file
          // TODO: Not working
          fs.unlinkSync(existFilePath);
          fs.renameSync(filePath, existFilePath);
        }
        result.status = "FAIL";
        result.description = `Screenshots are beyond maximum accepted variation: ${percentDiff.toFixed(2)}%.`;
        return result;
      } else {
        result.description = `Screenshots are within maximum accepted variation: ${percentDiff.toFixed(2)}%.`;
        fs.unlinkSync(filePath);
      }
    }

    if (step.overwrite == "true") {
      // Replace old file with new file
      fs.unlinkSync(existFilePath);
      fs.renameSync(filePath, existFilePath);
    }
  }

  // PASS
  return result;
}
```
  
  