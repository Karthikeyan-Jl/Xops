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
---

- **ConfigMap as env vars** ✅
  
<img width="1409" height="794" alt="Screenshot 2025-10-03 100337" src="https://github.com/user-attachments/assets/96924e50-bce7-4602-831c-1744ab200571" />

---

- **ConfigMap as mounted files** ✅

<img width="1109" height="145" alt="Screenshot 2025-10-03 100903" src="https://github.com/user-attachments/assets/4dac3c5c-96a0-4382-b6ad-49922ff42b5a" />

---

- **Secret as env vars** ✅

<img width="1055" height="265" alt="Screenshot 2025-10-03 101211" src="https://github.com/user-attachments/assets/ae23f6bd-90e3-4131-8279-8354ce5e1864" />

---
