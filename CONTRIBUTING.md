# Contributing to Kleff

> Build. Host. Scale. Your Way.

First off, thank you for taking the time to contribute! 💙  
Kleff is built on the belief that **hosting should be transparent, modular, and developer-driven**.  
This document outlines how you can help improve the platform.

---

## 🧠 Code of Conduct

Please review our [Code of Conduct](https://github.com/kleffio/.github/blob/main/CODE_OF_CONDUCT.md) before participating.  
We aim to maintain a welcoming and inclusive community for all developers.

---

## 🧱 How to Contribute

### 1. Fork the repository

Create your own fork of the repository you’d like to contribute to.

### 2. Create a new branch

Use a descriptive name for your branch:

```bash
git checkout -b feature/add-container-probes
```

### 3. Make your changes

Keep code modular, clean, and consistent with existing conventions.  
**Tips:**

- Keep commits small and meaningful.
- Reference issues or discussions in your commit messages.
- Include tests when possible.

### 4. Run linting and tests

Make sure your changes pass:

```sh
make test
make lint
```

### 5. Submit a Pull Request

Open a PR to the `main` branch and include:

- A concise description of what was added or fixed.
- Screenshots or logs if applicable.
- Reference to any related issue (`Fixes #123`).

Our maintainers will review it and provide feedback as soon as possible.

---

## 🧩 Style Guidelines

### Go (Backend)

- Follow idiomatic Go style (`go fmt` / `golangci-lint run`).
- Use `internal/` for non-exported packages.
- Keep architecture boundaries clear (API ↔ Business ↔ Infrastructure).

### TypeScript / React (Frontend)

- Follow ESNext + React 18 syntax.
- Use functional components and hooks.
- Keep styling consistent with Tailwind and ShadCN components.

---

## 🧪 Testing

We aim for **90 %+ coverage** across all critical modules.  
Please ensure your PR doesn't reduce coverage for major functions.

---

## 🤝 Community

Join our discussions, report bugs, or request features:

- [Issues](https://github.com/orgs/kleffio/discussions)
- [Email](mailto:kleffioapp@gmail.com)
- [Website](https://kleff.io)

Your feedback and ideas drive the future of Kleff 🚀

---

<p align="center">
  <b>Build. Host. Scale. Your Way.</b><br />
  <sub>Thank you for helping shape the Kleff ecosystem — every contribution matters.</sub><br />
  <sub>Licensed under the Kleff Public License v1.0 (based on Apache 2.0)</sub>
</p>
