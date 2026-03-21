# Security Policy

Kleff takes the security of its platform seriously. We appreciate the effort of security researchers and community members who responsibly disclose vulnerabilities, and we are committed to addressing them promptly and transparently.

---

## Supported Versions

We actively maintain security updates for the following:

| Version | Status |
|---------|--------|
| `main` (development branch) | Actively maintained |
| Latest stable release | Actively maintained |
| Previous stable release | Critical fixes only |
| Older versions | No longer supported |

We strongly recommend running the **latest stable release** or tracking `main` in development environments.

---

## Reporting a Vulnerability

**Do not open a public GitHub issue for security vulnerabilities.**
Public disclosure before a fix is available puts all Kleff users at risk.

### How to Report

Send a detailed report to: [kleffioapp@gmail.com](mailto:kleffioapp@gmail.com)

Your report should include:

- **Description** — A clear explanation of the vulnerability and its potential impact
- **Affected component** — Which service, endpoint, or configuration is affected (e.g., `platform`, `daemon`, `panel`, Helm chart)
- **Reproduction steps** — A minimal, reproducible test case or proof-of-concept if possible
- **Severity assessment** — Your estimate of impact (see severity levels below)
- **Suggested fix** — A proposed mitigation or patch, if you have one

### Response Timeline

| Milestone | Target |
|-----------|--------|
| Initial acknowledgment | Within 48 hours |
| Triage and severity assessment | Within 5 business days |
| Fix development complete | Depends on severity (see below) |
| Coordinated public disclosure | After fix is released |

---

## Severity Levels

We classify vulnerabilities using the following levels, aligned with CVSS conventions:

| Severity | Description | Target Fix Timeline |
|----------|-------------|---------------------|
| **Critical** | Remote code execution, authentication bypass, privilege escalation | 7 days |
| **High** | Significant data exposure, authorization bypass, container escape | 14 days |
| **Medium** | Information disclosure, limited-scope vulnerabilities | 30 days |
| **Low** | Minor issues, hardening recommendations | Next release cycle |

---

## Disclosure Process

1. The reporter submits a vulnerability report privately.
2. Maintainers acknowledge receipt and begin investigation.
3. A fix is developed and validated in a private branch.
4. A coordinated release is prepared, including a public security advisory (CVE if applicable).
5. The fix is released and the advisory is published.
6. The reporter is credited by name — or listed as anonymous, per their preference.

---

## Recognition

We believe responsible disclosure deserves public recognition. Contributors who report valid, previously unknown vulnerabilities will be:

- Credited in the public security advisory
- Listed in the release notes accompanying the fix

There is currently no formal bug bounty program, but we are genuinely grateful to every researcher who takes the time to disclose responsibly.

---

## Security Best Practices

When deploying Kleff in production:

- **Keep your cluster and Helm releases up to date** — security patches are released on a regular cadence.
- **Restrict API and dashboard access** — apply network policies, auth middleware, and firewall rules at every layer.
- **Enable TLS everywhere** — use Let's Encrypt and cert-manager for all public-facing endpoints.
- **Rotate secrets regularly** — especially API tokens, database credentials, and signing keys.
- **Scope Kubernetes RBAC tightly** — apply least-privilege principles to all service accounts and workloads.
- **Monitor audit logs** — Kleff emits structured audit events; route them to your SIEM or log aggregation pipeline.
- **Isolate tenant workloads** — use separate namespaces and network policies per tenant where your threat model requires it.

---

**Contact:** [kleffioapp@gmail.com](mailto:kleffioapp@gmail.com)
**Website:** [kleff.io](https://kleff.io)

---

<p align="center">
  <b>Build. Host. Scale. Your Way.</b><br />
  <sub>Security is a shared responsibility — thank you for helping keep Kleff safe for everyone.</sub>
</p>
