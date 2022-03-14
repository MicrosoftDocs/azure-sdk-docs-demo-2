---
title: Azure SDK for JavaScript - Key Vault User Guide
description: 
ms.topic: reference
ms.date: 02/10/2022
ms.service: key-vault
ms.role: developer
ms.devlang: javascript
author: DavidCBerry13
ms.author: daberry
ROBOTS: NOINDEX
---
# Azure KeyVaultManagement client library for JavaScript

This package contains an isomorphic SDK (runs both in Node.js and in browsers) for Azure KeyVaultManagement client.

The Azure management API provides a RESTful set of web services that interact with Azure Key Vault.

[Source code](https://github.com/Azure/azure-sdk-for-js/tree/main/sdk/keyvault/arm-keyvault) |
[Package (NPM)](https://www.npmjs.com/package/@azure/arm-keyvault) |
[API reference documentation](https://docs.microsoft.com/javascript/api/@azure/arm-keyvault) |
[Samples](https://github.com/Azure-Samples/azure-samples-js-management)

## Getting started

### Currently supported environments

- [LTS versions of Node.js](https://nodejs.org/about/releases/)
- Latest versions of Safari, Chrome, Edge and Firefox.

### Prerequisites

- An [Azure subscription][azure_sub].

### Install the `@azure/arm-keyvault` package

Install the Azure KeyVaultManagement client library for JavaScript with `npm`:

```bash
npm install @azure/arm-keyvault
```

### Create and authenticate a `KeyVaultManagementClient`

To create a client object to access the Azure KeyVaultManagement API, you will need the `endpoint` of your Azure KeyVaultManagement resource and a `credential`. The Azure KeyVaultManagement client can use Azure Active Directory credentials to authenticate.
You can find the endpoint for your Azure KeyVaultManagement resource in the [Azure Portal][azure_portal].

You can authenticate with Azure Active Directory using a credential from the [@azure/identity][azure_identity] library or [an existing AAD Token](https://github.com/Azure/azure-sdk-for-js/blob/master/sdk/identity/identity/samples/AzureIdentityExamples.md#authenticating-with-a-pre-fetched-access-token).

To use the [DefaultAzureCredential][defaultazurecredential] provider shown below, or other credential providers provided with the Azure SDK, please install the `@azure/identity` package:

```bash
npm install @azure/identity
```

You will also need to **register a new AAD application and grant access to Azure KeyVaultManagement** by assigning the suitable role to your service principal (note: roles such as `"Owner"` will not grant the necessary permissions).
Set the values of the client ID, tenant ID, and client secret of the AAD application as environment variables: `AZURE_CLIENT_ID`, `AZURE_TENANT_ID`, `AZURE_CLIENT_SECRET`.

For more information about how to create an Azure AD Application check out [this guide](https://docs.microsoft.com/azure/active-directory/develop/howto-create-service-principal-portal).

```javascript
const { KeyVaultManagementClient } = require("@azure/arm-keyvault");
const { DefaultAzureCredential } = require("@azure/identity");
const subscriptionId = "00000000-0000-0000-0000-000000000000";
const client = new KeyVaultManagementClient(new DefaultAzureCredential(), subscriptionId);
```


### JavaScript Bundle
To use this client library in the browser, first you need to use a bundler. For details on how to do this, please refer to our [bundling documentation](https://aka.ms/AzureSDKBundling).

## Key concepts

### KeyVaultManagementClient

`KeyVaultManagementClient` is the primary interface for developers using the Azure KeyVaultManagement client library. Explore the methods on this client object to understand the different features of the Azure KeyVaultManagement service that you can access.

## Troubleshooting

### Logging

Enabling logging may help uncover useful information about failures. In order to see a log of HTTP requests and responses, set the `AZURE_LOG_LEVEL` environment variable to `info`. Alternatively, logging can be enabled at runtime by calling `setLogLevel` in the `@azure/logger`:

```javascript
const { setLogLevel } = require("@azure/logger");
setLogLevel("info");
```

For more detailed instructions on how to enable logs, you can look at the [@azure/logger package docs](https://github.com/Azure/azure-sdk-for-js/tree/main/sdk/core/logger).

## Next steps

Please take a look at the [samples](https://github.com/Azure-Samples/azure-samples-js-management) directory for detailed examples on how to use this library.

## Contributing

If you'd like to contribute to this library, please read the [contributing guide](https://github.com/Azure/azure-sdk-for-js/blob/main/CONTRIBUTING.md) to learn more about how to build and test the code.

## Related projects

- [Microsoft Azure SDK for JavaScript](https://github.com/Azure/azure-sdk-for-js)

![Impressions](https://azure-sdk-impressions.azurewebsites.net/api/impressions/azure-sdk-for-js%2Fsdk%2Fkeyvault%2Farm-keyvault%2FREADME.png)

[azure_cli]: https://docs.microsoft.com/cli/azure
[azure_sub]: https://azure.microsoft.com/free/
[azure_sub]: https://azure.microsoft.com/free/
[azure_portal]: https://portal.azure.com
[azure_identity]: https://github.com/Azure/azure-sdk-for-js/tree/main/sdk/identity/identity
[defaultazurecredential]: https://github.com/Azure/azure-sdk-for-js/tree/main/sdk/identity/identity#defaultazurecredential