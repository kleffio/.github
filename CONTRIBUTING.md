# Contributing to Kleff

> Build. Host. Scale. Your Way.

Thank you for your interest in contributing to Kleff. This project is built on the belief that **hosting infrastructure should be transparent, modular, and developer-controlled** — and that only happens with a strong community behind it.

Please read this document in full before opening your first issue or pull request. It helps us keep the codebase high-quality and the review process efficient for everyone.

---

## Code of Conduct

By participating in this project, you agree to abide by the [Kleff Code of Conduct](./CODE_OF_CONDUCT.md). We are committed to maintaining a respectful, inclusive, and professional community.

---

## Ways to Contribute

You don't have to write code to make a meaningful contribution. We welcome:

- **Bug reports** — Clear, reproducible reports with relevant environment and version details
- **Feature requests** — Thoughtful proposals with use-case context and problem framing
- **Documentation** — Improvements to guides, architecture docs, READMEs, and inline comments
- **Code contributions** — Bug fixes, features, performance improvements, and targeted refactors
- **Security reports** — Responsible disclosure via our [Security Policy](./SECURITY.md)
- **Community participation** — Helping others in discussions, issues, and code review threads

---

## Getting Started

### Prerequisites

| Tool | Minimum Version |
|------|----------------|
| Go | 1.23+ |
| Node.js | 20+ |
| Docker | 24+ |
| Make | any |

### Development Setup

```bash
# 1. Fork and clone the repository you want to work on
git clone https://github.com/<your-org>/kleff.git
cd kleff

# 2. Start the full development stack
docker compose -f App/docker-compose.dev.yml up -d

# 3. Run a service locally (example: platform)
cd App/platform
make run
```

Refer to each subdirectory's `README.md` for service-specific setup instructions and environment variables.

---

## Contribution Workflow

### 1. Open or find an issue

Before writing code, check whether an existing issue covers what you want to address. For any significant change — new features, architectural decisions, or behavior modifications — open an issue first to discuss your approach with the maintainers before investing time in implementation.

### 2. Fork and create a branch

Work on a personal fork and create a branch with a descriptive, prefixed name:

```bash
git checkout -b feat/node-federation
git checkout -b fix/container-probe-timeout
git checkout -b docs/update-security-policy
```

**Branch naming convention:**

| Prefix | Purpose |
|--------|---------|
| `feat/` | New features |
| `fix/` | Bug fixes |
| `docs/` | Documentation only |
| `chore/` | Maintenance, dependencies, configuration |
| `refactor/` | Structural changes without behavior change |
| `test/` | Test additions or fixes |

### 3. Make your changes

- Keep commits small, focused, and independently reviewable.
- Reference related issues in commit messages.
- Do not mix unrelated changes in a single PR.

### 4. Follow commit message conventions

We follow the [Conventional Commits](https://www.conventionalcommits.org) specification:

```
<type>(<scope>): <short summary>

[optional body]

[optional footer: Fixes #123]
```

**Examples:**

```
feat(platform): add node federation endpoint
fix(daemon): resolve container probe timeout on startup
docs(security): clarify responsible disclosure timeline
chore(deps): bump golangci-lint to v1.57.0
```

### 5. Test your changes

Before submitting, ensure all checks pass:

```bash
make test    # Run unit and integration tests
make lint    # Run all linters
```

We aim for **90%+ coverage** on all critical modules. Pull requests that reduce coverage on core components will be flagged during review.

### 6. Open a Pull Request

Target the `main` branch and fill out the provided PR template. Include:

- A clear summary of what was changed and why
- A reference to the related issue (`Fixes #123` or `Closes #456`)
- Screenshots or log output where applicable
- Any migration, deployment, or breaking change notes

A maintainer will review your PR and either approve, request changes, or close it with an explanation.

---

## Code Style

### Go (Backend)

- Follow idiomatic Go — run `go fmt` and `golangci-lint run` before submitting.
- Use `internal/` for packages that are not part of the public API surface.
- Respect hexagonal architecture boundaries: adapters → application → domain. Dependencies must not flow outward.
- Avoid global state. Prefer dependency injection and explicit interfaces.
- Keep error handling explicit — do not swallow or silently discard errors.

### TypeScript / React (Frontend)

- Use ESNext + React 19 syntax and conventions.
- Prefer functional components and hooks over class components.
- Keep styling consistent with Tailwind CSS and ShadCN UI conventions.
- Avoid inline styles; use utility classes.
- Colocate component tests in `__tests__/` directories adjacent to the component.

---

## Documentation

- Update documentation alongside code changes wherever relevant.
- Architecture documentation lives in `ARCHITECTURE.md` files at the repository and service level.
- Use clear, direct language. Avoid domain jargon unless it is standard and well-understood.

---

## What We Are Not Looking For

To keep review cycles efficient and the codebase focused, please avoid:

- Large, unfocused pull requests that mix features, fixes, and refactors
- Core architecture changes without prior discussion in an issue
- Adding dependencies without a well-justified use case
- Removing tests or lowering coverage to make a PR pass
- Cosmetic-only changes to files that were not otherwise necessary to touch

---

## Security Contributions

If your contribution touches authentication, authorization, container isolation, networking, or any other security-sensitive area, review the [Security Policy](./SECURITY.md) before proceeding.

**Do not disclose security vulnerabilities via public issues or pull requests.**

---

## Community

- [GitHub Discussions](https://github.com/orgs/kleffio/discussions) — ideas, questions, and architectural proposals
- [Issues](https://github.com/kleffio/.github/issues) — bug reports and feature requests
- [Email](mailto:kleffioapp@gmail.com) — direct contact with maintainers
- [Website](https://kleff.io)

---

<p align="center">
  <b>Build. Host. Scale. Your Way.</b><br />
  <sub>Thank you for helping shape the Kleff ecosystem — every contribution matters.</sub>
</p>
