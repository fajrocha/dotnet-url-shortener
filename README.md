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

```bash
az deployment group what-if --resource-group appdev-rg-prd-we-dotnet-urlshortener --template-file infrastructure/main.bicep
```

### Deploy

```bash
az deployment group create --resource-group appdev-rg-prd-we-dotnet-urlshortener --template-file infrastructure/main.bicep
```
