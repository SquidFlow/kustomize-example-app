## Configuration Details

- Base configurations are in the `base` directory
- Environment-specific configurations are in respective directories under `overlays`
- Each environment can customize:
  - Resource name prefix
  - Namespace
  - Number of replicas
  - Other environment-specific parameters

## Template Usage

```shell
# Build and preview the resources for SIT environment
kustomize build overlays/sit

# Build and preview the resources for UAT environment
kustomize build overlays/uat

# Build and directly apply to kubernetes cluster
kustomize build overlays/sit | kubectl apply -f -

# Build and validate the output without applying
kustomize build overlays/sit | kubectl apply -f - --dry-run=client

# View differences before applying
kustomize build overlays/sit | kubectl diff -f -
```

## Important Notes

1. Ensure kubectl is installed and properly configured
2. Always use dry-run before actual deployment
3. Verify target namespaces exist before deployment