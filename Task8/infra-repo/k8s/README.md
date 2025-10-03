# XOps Microchallenge #8 – ConfigMaps vs Secrets

## ConfigMaps
- Store **non-sensitive configuration** such as environment settings, feature flags, app properties.
- Example: `APP_MODE=dev`, `FEATURE_X_ENABLED=true`.
- Can be injected as:
  - Environment variables
  - Mounted as files

## Secrets
- Store **sensitive data** such as credentials, tokens, API keys.
- Data is base64-encoded (not encrypted by default).
- Can also be injected as env vars or mounted as files.
- Should be encrypted at rest using KMS.

## Best Practices
✅ Use ConfigMaps for non-sensitive app configs  
✅ Use Secrets for passwords, tokens, certificates  
✅ Do not hardcode sensitive info in ConfigMaps  
✅ Enable encryption at rest for Secrets  
✅ Restrict RBAC access to Secrets  

## Verification
- **ConfigMap as env vars** ✅

- **ConfigMap as mounted files** ✅

- **Secret as env vars** ✅
