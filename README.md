# Kleff — `.github` Repository

> *Build. Host. Scale. Your Way.*

This repository is the central source of truth for community governance, contribution standards, and organization-wide documentation across the Kleff ecosystem.

---

## Purpose

The `.github` repository defines how the Kleff community operates, collaborates, and contributes across all projects within the organization. Files stored here are automatically recognized by GitHub and applied as defaults across every repository under the `kleffio` organization.

| File | Description |
|------|-------------|
| [`profile/README.md`](./profile/README.md) | Public-facing README displayed on the [Kleff GitHub Organization](https://github.com/kleffio) page |
| [`CODE_OF_CONDUCT.md`](./CODE_OF_CONDUCT.md) | Community standards for respectful and inclusive participation |
| [`CLA.md`](./CLA.md) | Contributor License Agreement — required to be signed before any contribution is merged |
| [`LICENSE`](./LICENSE) | The MIT License governing all open-source repositories |

---

## How Community Health Files Work

GitHub automatically applies files from a `.github` repository as organization-wide defaults for any repository that does not define its own. This means:

- **Code of Conduct** applies globally by default.
- Individual repositories may override these by including their own copies at the root level.
- The `profile/README.md` is rendered publicly on the organization's main GitHub page.
- Workflow templates and issue/PR templates added here are available across all Kleff repositories.

---

## Contributor License Agreement (CLA)

**All contributors must sign the CLA before any pull request can be merged.** This applies to every repository in the `kleffio` organization without exception.

The CLA check is enforced via the reusable [`_cla`](./.github/workflows/_cla.yml) workflow. Each repository must call this workflow on pull request events. Signing is done automatically via a comment on the pull request the first time a contributor opens one.

To call the CLA workflow from any repository:

```yaml
name: CLA
on:
  pull_request_target:
    types: [opened, synchronize]
  issue_comment:
    types: [created]

jobs:
  cla:
    uses: kleffio/.github/.github/workflows/_cla.yml@main
    secrets:
      personal_access_token: ${{ secrets.CLA_PERSONAL_ACCESS_TOKEN }}
```

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

## License

This project is licensed under the **MIT License**.
See the [LICENSE](./LICENSE) file for full terms and conditions.

---

<p align="center">
  <b>Build. Host. Scale. Your Way.</b><br />
  <sub>© 2025 Kleff Hosting — Open Source by <a href="https://github.com/isaacwallace123">Isaac Wallace</a></sub><br />
  <sub>Licensed under the MIT License</sub>
</p>
