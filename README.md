# Kleff — `.github` Repository

> *Build. Host. Scale. Your Way.*

This repository is the central source of truth for community governance, contribution standards, and organization-wide documentation across the Kleff ecosystem.

---

## Purpose

The `.github` repository defines how the Kleff community operates, collaborates, and contributes across all projects within the organization. Files stored here are automatically recognized by GitHub and applied as defaults across every repository under the `kleffio` organization.

| File | Description |
|------|-------------|
| [`profile/README.md`](./profile/README.md) | Public-facing README displayed on the [Kleff GitHub Organization](https://github.com/kleffio) page |
| [`CONTRIBUTING.md`](./CONTRIBUTING.md) | Contribution guidelines, workflow, branch conventions, and code style |
| [`CODE_OF_CONDUCT.md`](./CODE_OF_CONDUCT.md) | Community standards for respectful and inclusive participation |
| [`SECURITY.md`](./SECURITY.md) | Responsible disclosure policy, severity levels, and vulnerability reporting |
| [`VISION.md`](./VISION.md) | Long-term goals, guiding principles, and ecosystem roadmap |
| [`LICENSE`](./LICENSE) | The Kleff Public License v1.0 governing all open-source repositories |
| [`TRADEMARKS.md`](./TRADEMARKS.md) | Trademark usage guidelines for the Kleff name and branding |

---

## How Community Health Files Work

GitHub automatically applies files from a `.github` repository as organization-wide defaults for any repository that does not define its own. This means:

- **Code of Conduct**, **Contributing**, and **Security** policies apply globally by default.
- Individual repositories may override these by including their own copies at the root level.
- The `profile/README.md` is rendered publicly on the organization's main GitHub page.
- Workflow templates and issue/PR templates added here are available across all Kleff repositories.

---

## Ecosystem

Kleff is an open-source hosting platform for web servers, game servers, and containerized workloads. The core components are:

| Repository | Description |
|------------|-------------|
| [kleffio/platform](https://github.com/kleffio/platform) | Go backend control plane — API, auth, state management, event dispatch |
| [kleffio/panel](https://github.com/kleffio/panel) | Next.js + TypeScript management dashboard |
| [kleffio/gameserver-daemon](https://github.com/kleffio/gameserver-daemon) | Node-level daemon for container runtime management |
| [kleffio/argocd](https://github.com/kleffio/argocd) | GitOps / ArgoCD application definitions for Kubernetes delivery |

---

## Contributing

Please review the [Contributing Guide](./CONTRIBUTING.md) before opening issues or pull requests. All participation in the Kleff community is governed by the [Code of Conduct](./CODE_OF_CONDUCT.md).

To propose changes to organization-wide policies or documentation, open an issue or pull request in this repository. For broader project discussions, use [GitHub Discussions](https://github.com/orgs/kleffio/discussions).

---

## Security

If you discover a vulnerability, follow the [Security Policy](./SECURITY.md) for responsible disclosure.
**Do not open public issues for security vulnerabilities.**

---

## License

This project is licensed under the **Kleff Public License v1.0** (based on Apache 2.0).
See the [LICENSE](./LICENSE) file for full terms and conditions.

---

<p align="center">
  <b>Build. Host. Scale. Your Way.</b><br />
  <sub>© 2025 Kleff Hosting — Open Source by <a href="https://github.com/isaacwallace123">Isaac Wallace</a></sub><br />
  <sub>Licensed under the Kleff Public License v1.0 (based on Apache 2.0)</sub>
</p>
