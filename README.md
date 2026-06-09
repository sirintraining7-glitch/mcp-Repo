# mcp-Repo

Minimal Node.js web app with GitHub Actions CI/CD deploying to Azure App Service.

Getting started

1. Install dependencies

```bash
npm ci
```

2. Run locally

```bash
npm start
```

3. Tests

```bash
npm test
```

Required GitHub Secrets for CI/CD

- `AZURE_CREDENTIALS` — service principal JSON for `azure/login` (see `az ad sp create-for-rbac --sdk-auth`)
- `AZURE_RESOURCE_GROUP` — target resource group name
- `AZURE_WEBAPP_NAME` — desired App Service name
- `AZURE_WEBAPP_URL` — public URL (e.g., https://<app-name>.azurewebsites.net)

Infra

The repo contains `infra/main.bicep` which provisions an App Service Plan and Linux Web App.
