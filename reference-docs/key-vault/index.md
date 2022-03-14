---
title: Azure SDK for JavaScript - Key Vault packages
description: 
ms.topic: reference
ms.date: 02/10/2022
ms.service: key-vault
ms.role: developer
ms.devlang: javascript
author: DavidCBerry13
ms.author: daberry
---

# Azure SDK for JavaScript - Key Vault packages

[Azure Key Vault](https://azure.microsoft.com/services/key-vault/) is a Microsoft-managed service providing cloud keys, secrets, and certificate storage and utility that is highly available, secure, durable, scalable, and redundant.

The current Azure SDK for JavaScript contains four packages for interacting with Azure Key Vault from your application.
- **Key Vault Admin** - Used to get, set, list, and delete Azure RBAC (Role-Based Access Control) role assignments and definitions within a key vault.
- **Key Vault Certificates** - Used to get, set, update, and delete certificates in a key vault.
- **Key Vault Keys** - Used to create, import, update, and delete cryptographic keys in a key vault.
- **Key Vault Secrets** - Used to get, set, update, and delete application secrets (connection strings, api keys, etc.) in a key vault.

The package `azure-keyvault` is now considered a legacy package. New applications should not be developed using this package.  Current users of this package should migrate to the Key Vault Certificates, Key Vault Keys, and Key Vault Secrets packages as appropriate. The following migration guides are available to aid in this migration.
- [Guide for migrating to @azure/keyvault-certificates from azure-keyvault](/azure/javascript/sdk/sdk-demo2/key-vault/azure-keyvault-certificates/migration-guide?branch=main)
- [Guide for migrating to @azure/keyvault-keys from azure-keyvault](/azure/javascript/sdk/sdk-demo2/key-vault/azure-keyvault-keys/migration-guide?branch=main)
- [Guide for migrating to @azure/keyvault-secrets from azure-keyvault](/azure/javascript/sdk/sdk-demo2/key-vault/azure-keyvault-secrets/migration-guide?branch=main)

## Stable packages

| Name                  | Package              | Version          | Reference Docs         | Package Manager                |
|-----------------------|----------------------|------------------|------------------------|--------------------------------|
| Key Vault - Admin | @azure/keyvault-admin | 4.1.0 | [docs](/azure/javascript/sdk/sdk-demo2/key-vault/azure-keyvault-admin/stable)  | npm [4.1.0](https://www.npmjs.com/package/%40azure%2Fkeyvault-admin) |
| Key Vault - Certificates | @azure/keyvault-certificates | 4.3.0 | [docs](/azure/javascript/sdk/sdk-demo2/key-vault/azure-keyvault-certificates/stable)  | npm [4.3.0](https://www.npmjs.com/package/%40azure%2Fkeyvault-certificates) |
| Key Vault - Keys | @azure/keyvault-keys | 4.3.0 | [docs](/azure/javascript/sdk/sdk-demo2/key-vault/azure-keyvault-keys/stable)  | npm [4.3.0](https://www.npmjs.com/package/%40azure%2Fkeyvault-keys) |
| Key Vault - Secrets | @azure/keyvault-secrets | 4.3.0 | [docs](/azure/javascript/sdk/sdk-demo2/key-vault/azure-keyvault-secrets/stable)  | npm [4.3.0](https://www.npmjs.com/package/%40azure%2Fkeyvault-secrets) |
| Key Vault - Resource Management | @azure/arm-keyvault | 2.0.0 | [docs](/azure/javascript/sdk/sdk-demo2/key-vault/azure-arm-keyvault/stable)  | npm [2.0.0](https://www.npmjs.com/package/%40azure%2Farm-keyvault) |
 

## Beta packages

| Name                  | Package              | Version          | Reference Docs         | Package Manager                |
|-----------------------|----------------------|------------------|------------------------|--------------------------------|
| Key Vault - Admin | @azure/keyvault-admin | 4.2.0-beta.2 | [docs](/azure/javascript/sdk/sdk-demo2/key-vault/azure-keyvault-admin/beta)  | npm [4.2.0-beta.2](https://www.npmjs.com/package/%40azure%2Fkeyvault-admin%404.2.0-beta.2) |
| Key Vault - Certificates | @azure/keyvault-certificates | 4.4.0-beta.2 | [docs](/azure/javascript/sdk/sdk-demo2/key-vault/azure-keyvault-certificates/beta)  | npm [4.4.0-beta.2](https://www.npmjs.com/package/%40azure%2Fkeyvault-certificates%404.4.0-beta.2) |
| Key Vault - Keys | @azure/keyvault-keys | 4.4.0-beta.4 | [docs](/azure/javascript/sdk/sdk-demo2/key-vault/azure-keyvault-keys/beta)  | npm [4.4.0-beta.4](https://www.npmjs.com/package/%40azure%2Fkeyvault-keys%404.4.0-beta.4) |
| Key Vault - Secrets | @azure/keyvault-secrets | 4.4.0-beta.2 | [docs](/azure/javascript/sdk/sdk-demo2/key-vault/azure-keyvault-secrets/beta)  | npm [4.4.0-beta.2](https://www.npmjs.com/package/%40azure%2Fkeyvault-secrets%404.4.0-beta.2) |
 


## Legacy packages

| Name                  | Package              | Version          | Reference Docs         | Package Manager                |
|-----------------------|----------------------|------------------|------------------------|--------------------------------|
| Key Vault | azure-keyvault | 3.0.5 | [docs](/azure/javascript/sdk/sdk-demo2/key-vault/legacy/azure-keyvault/legacy)  | npm [3.0.5](https://www.npmjs.com/package/azure-keyvault%403.0.5) |
| Key Vault - Resource Management | azure-arm-keyvault | 1.2.0 | [docs](/azure/javascript/sdk/sdk-demo2/key-vault/legacy/azure-arm-keyvault/legacy)  | npm [1.2.0](https://www.npmjs.com/package/azure-arm-keyvault%401.2.0) |
 