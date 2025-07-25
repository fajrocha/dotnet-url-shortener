# dotnet-url-shortener

## Infrastructure as Code

### Download Azure CLI

https://learn.microsoft.com/en-us/cli/azure/

### Log in into Azure

```bash
az login
```

### Create Resource Group

```bash
az group create --name appdev-rg-prd-we-dotnet-urlshortener --location westeurope
```

### Deploy Bicep

### What if

To get a preview of the _Azure_ resources to be created.

```bash
az deployment group what-if --resource-group appdev-rg-prd-we-dotnet-urlshortener --template-file infrastructure/main.bicep
```

### Deploy

```bash
az deployment group create --resource-group appdev-rg-prd-we-dotnet-urlshortener --template-file infrastructure/main.bicep
```

### Create User for GH Actions

```bash
az ad sp create-for-rbac --name "GitHub-Actions-SP" `
                         --role contributor `
                         --scopes /subscriptions/86c784c6-6555-4bac-8d1e-a7295191bef7 `
                         --sdk-auth
```
