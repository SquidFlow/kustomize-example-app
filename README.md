## Configuration Details

- Base configurations are in the `base` directory
- Environment-specific configurations are in respective directories under `overlays`
- Each environment can customize:
  - Resource name prefix
  - Namespace
  - Number of replicas
  - Other environment-specific parameters

## Important Notes

1. Ensure kubectl is installed and properly configured
2. Always use dry-run before actual deployment
3. Verify target namespaces exist before deployment