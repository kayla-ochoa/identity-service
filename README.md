# Identity API — README.md

## Overview

The Identity API manages users and identity lookups. It is deployed into a shared Kubernetes cluster orchestrated by the `accounts-api` repository.

### Endpoints

* POST `/users`
* GET `/users/:id`
* GET `/users`
* GET `/health`

### Local Development

```bash
npm install
npm run dev
```

Default port: `3001`

Health check:

```bash
curl http://localhost:3001/health
```

### Kubernetes

Defines:

* Namespace: `identity`
* Deployment: `identity-api`
* Service: `identity-api`

Cluster creation, ingress, and Insights agent installation are handled by `accounts-api`.
