
  
   # **Suggest**

## What does this do?

The `suggest` method suggests actions based on the user's input. It takes an array of intents as input and returns an array of suggested actions.

## Why should I use this?

The `suggest` method can be used to provide users with suggestions for what they can do next. This can be helpful in a variety of situations, such as when a user is stuck or when they are looking for new ways to use your product.

## Prerequisites

There are no prerequisites for using the `suggest` method.

## How to use this

To use the `suggest` method, simply pass an array of intents as input. The method will then return an array of suggested actions.

Here is an example of how to use the `suggest` method:

```
const intents = ['search', 'play', 'settings'];
const actions = suggest(intents);

console.log(actions);
```

The output of the above code would be:

```
[
  'Search for something',
  'Play a game',
  'Open the settings menu'
]
```

## Example

The following code shows you how to use the `suggest` method to provide users with suggestions for what they can do next:

```
const intents = ['search', 'play', 'settings'];
const actions = suggest(intents);

const suggestions = actions.map(action => {
  return {
    title: action,
    description: `This action will ${action.toLowerCase()}.`
  };
});

console.log(suggestions);
```

The output of the above code would be:

```
[
  {
    title: 'Search for something',
    description: 'This action will search for something.'
  },
  {
    title: 'Play a game',
    description: 'This action will play a game.'
  },
  {
    title: 'Open the settings menu',
    description: 'This action will open the settings menu.'
  }
]
```
  
  