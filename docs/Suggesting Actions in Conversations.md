
  
   # **Suggest**

## What does this do?

The `suggest` method suggests actions based on the current state of the conversation.

## Why should I use this?

The `suggest` method can be used to provide users with suggestions for what to do next in a conversation. This can be helpful for guiding users through a complex conversation or for providing them with options for how to proceed.

## Prerequisites

There are no prerequisites for using the `suggest` method.

## How to use this

To use the `suggest` method, you must first create a `Match` object. A `Match` object represents a possible action that the user can take in a conversation. You can create a `Match` object by calling the `match` method on a `Conversation` object.

Once you have created a `Match` object, you can add it to the `actions` array of a `Suggest` object. You can then call the `suggest` method on a `Conversation` object to send the `Suggest` object to the user.

The following code sample shows you how to use the `suggest` method:

```javascript
const conversation = new Conversation();

const match = conversation.match('What is the weather today?');

const suggest = new Suggest();
suggest.actions.push(match);

conversation.suggest(suggest);
```

## Example

The following example shows you how the `suggest` method can be used to provide users with suggestions for what to do next in a conversation.

```javascript
const conversation = new Conversation();

const match1 = conversation.match('What is the weather today?');
const match2 = conversation.match('What is the time?');
const match3 = conversation.match('What is the news?');

const suggest = new Suggest();
suggest.actions.push(match1);
suggest.actions.push(match2);
suggest.actions.push(match3);

conversation.suggest(suggest);
```

In this example, the `suggest` method will send the user a list of three suggestions: "What is the weather today?", "What is the time?", and "What is the news?". The user can then choose one of these suggestions to continue the conversation.
  
  