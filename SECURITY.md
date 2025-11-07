# Kleff Security Policy

## Supported Versions

The following branches and releases receive active security updates:

| Version | Supported |
|----------|------------|
| main (development) | ✅ Yes |
| latest stable release | ✅ Yes |
| previous stable release | ⚠️ Critical fixes only |
| older versions | ❌ No longer supported |

We recommend always running the **latest stable image or Helm release**.

---

## Reporting a Vulnerability

If you discover a security vulnerability in any Kleff service, package, or deployment file:

1. **Do not open a public issue.**  
   Responsible disclosure keeps the community safe.
2. **Email:** [kleffioapp@gmail.com](mailto:kleffioapp@gmail.com)  
   Include:
   - A clear description of the issue and potential impact  
   - Steps to reproduce (if applicable)  
   - A suggested mitigation or patch (if available)

You will receive an acknowledgment within **48 hours**, and a follow-up once the vulnerability has been validated and prioritized.

---

## Disclosure Process

- The maintainers will investigate and confirm the issue.  
- A fix will be developed and tested in a private branch.  
- A coordinated release will be made with a public advisory.  
- You will be credited for responsible disclosure (unless you prefer anonymity).

---

## Security Best Practices

When running Kleff in production:

- Keep your cluster and Helm releases **up to date**.  
- Restrict API and dashboard access with **network policies** and **auth middleware**.  
- Use **TLS (Let’s Encrypt / cert-manager)** for all public endpoints.  
- Rotate secrets regularly.  
- Limit service permissions and Kubernetes RBAC scopes.  

---

**Contact:** [kleffioapp@gmail.com](mailto:kleffioapp@gmail.com)  
**Website:** [https://kleff.io](https://kleff.io)

> _Build. Host. Scale. Your Way._  
> Security is a shared responsibility — thank you for helping keep Kleff safe for everyone.
