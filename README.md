# GitOps Tests

This repository contains GitOps configurations for managing Kubernetes resources.

## Structure

```
.
├── apps/                    # ArgoCD Application definitions
│   └── dummy-namespace-app.yaml
└── manifests/               # Kubernetes resource manifests
    └── dummy-namespace/
        └── namespace.yaml
```

## Applications

### Dummy Namespace

Creates a dummy namespace in the Kubernetes cluster.

**Application:** `apps/dummy-namespace-app.yaml`
**Manifests:** `manifests/dummy-namespace/`

## Usage

### With ArgoCD

1. Update the `repoURL` in `apps/dummy-namespace-app.yaml` to point to your Git repository
2. Apply the Application manifest to your ArgoCD cluster:
   ```bash
   kubectl apply -f apps/dummy-namespace-app.yaml
   ```

### Direct Apply

You can also apply the manifests directly:
```bash
kubectl apply -f manifests/dummy-namespace/
```

## Requirements

- Kubernetes cluster
- ArgoCD (for GitOps workflow)
- kubectl configured to access your cluster

