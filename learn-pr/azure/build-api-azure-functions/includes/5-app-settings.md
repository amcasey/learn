You're working on an API that connects to a database. Your API will connect to that database via a database connection string. In this module, you'll learn best practices for storing sensitive information like connection strings in an Azure Functions API.

## Store connection strings in Azure Functions

It's a good idea to avoid hard-coding connection strings. You'll likely use the connection string across different files, and there's a chance that it could change in the future.

You'll want to store the connection string as an app setting. App settings are specified in one place and referenced throughout the app. You can easily change them at any point in the future without having to change the code. App settings are never checked in to source control.

An Azure Functions project has a `local.settings.json` file. This file contains a set of key/value pairs the app uses as configuration values. You can add your own items to the `Values` object. You can access those values from your code.

```json
{
  "IsEncrypted": false,
  "Values": {
    "AzureWebJobsStorage": "",
    "FUNCTIONS_WORKER_RUNTIME": "node"
  }
}
```

If you want to add a connection string, you can add another property called "CONNECTION_STRING" (or whatever you'd like to call it), and then pass the connection string to your database.

```json
{
  "IsEncrypted": false,
  "Values": {
    "AzureWebJobsStorage": "",
    "FUNCTIONS_WORKER_RUNTIME": "node",
    "CONNECTION_STRING": "AccountEndpoint=https://tailwind-traders-7983.documents.azure.com:443/;AccountKey=DQRvPibrRolFNVoVjyV8s4kBHr3jlixSBTVVJuwCMxG7NSeBmaftVuaXQ3Hi5h4Dw1AQXB0x1jdIqqBw1ZYzUQ==;"
  }
}
```

## Access app settings in Azure Functions code

To access these configuration values in your Azure Functions from JavaScript, see the `process.env` object. It contains all of the key/value pairs that are specified in the `local.settings.json` file.

```typescript
let client = new CosmosClient(process.env.CONNECTION_STRING);
```

You now know how to securely store a connection string, and how to reference that string in your application.
