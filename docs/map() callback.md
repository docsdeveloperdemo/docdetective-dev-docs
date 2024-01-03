
  
   # **Suggest**

## What does this do?

The `suggest` method suggests a list of possible completions for the given input.

## Why should I use this?

The `suggest` method can be used to provide auto-complete functionality for a text editor or IDE. It can also be used to provide suggestions for search queries or other text input fields.

## Prerequisites

To use the `suggest` method, you must have a valid API key. You can get an API key by creating an account on the [Google Cloud Platform](https://console.cloud.google.com/).

## How to use this

To use the `suggest` method, you must first create a `SuggestClient`. You can do this by calling the `SuggestClient.create()` method.

Once you have created a `SuggestClient`, you can call the `suggest()` method to get a list of suggested completions. The `suggest()` method takes the following parameters:

* `input`: The input text for which you want to get suggestions.
* `languageCode`: The language code of the input text.
* `maxSuggestions`: The maximum number of suggestions to return.

The `suggest()` method returns a list of `Suggestion` objects. Each `Suggestion` object contains the following fields:

* `suggestion`: The suggested completion.
* `score`: The score of the suggestion. The score is a number between 0 and 1, where 1 indicates a perfect match.

You can use the `score` field to rank the suggestions and display the most relevant suggestions to the user.

Here is an example of how to use the `suggest` method:

```javascript
const {SuggestClient} = require('@google-cloud/documentai').v1;

// Instantiates a client
const client = new SuggestClient();

async function callSuggest() {
  // Construct request
  const request = {
    parent: 'projects/YOUR_PROJECT_ID/locations/YOUR_LOCATION_ID',
    input: 'Hello, world!',
    languageCode: 'en-US',
    maxSuggestions: 5,
  };

  // Run request
  const [response] = await client.suggest(request);

  console.log(response);
}

callSuggest();

```
  
  