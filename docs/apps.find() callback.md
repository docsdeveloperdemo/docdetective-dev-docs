
  
   # **App**

## What does this do?

The `App` class represents a single application that can be managed by the DocDetective service.

## Why should I use this?

The `App` class provides a way to manage the applications that are being monitored by the DocDetective service. This can be useful for organizing and tracking the applications that are being monitored, as well as for managing the permissions that are granted to users for each application.

## Prerequisites

In order to use the `App` class, you must first create a DocDetective account and obtain an API key. You can then use the API key to authenticate your requests to the DocDetective API.

## How to use this

To use the `App` class, you can follow these steps:

1. Create an instance of the `App` class.
2. Set the `name` and `path` properties of the `App` instance.
3. Call the `save()` method of the `App` instance to save the app to the DocDetective service.

The following code sample shows how to use the `App` class:

```javascript
const app = new App();
app.name = 'My App';
app.path = '/my-app';
app.save();
```

## Example

The following code sample shows how to use the `App` class to manage the applications that are being monitored by the DocDetective service:

```javascript
// Create a DocDetective client.
const client = new DocDetectiveClient();

// Create an instance of the App class.
const app = new App();
app.name = 'My App';
app.path = '/my-app';

// Save the app to the DocDetective service.
await client.saveApp(app);

// Get all of the apps that are being monitored by the DocDetective service.
const apps = await client.getApps();

// Print the names of all of the apps.
for (const app of apps) {
  console.log(app.name);
}
```
  
  