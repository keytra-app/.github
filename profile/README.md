# Keytra

**Minimalist, self-hosted, open-source localization platform built for developer workflows.**

Keytra strips away the enterprise bloat of traditional translation management systems. JSON-first, zero SMTP required, keyboard-driven dark UI, and up and running in 60 seconds with Docker Compose.

### Repositories

| Repository | Description | Links |
| :--- | :--- | :--- |
| **[keytra](https://github.com/keytra-app/keytra)** | Self-hosted translation management platform (Next.js, Drizzle ORM, PostgreSQL, Docker) | [Docker Image (GHCR)](https://github.com/keytra-app/keytra/pkgs/container/keytra) · [Releases](https://github.com/keytra-app/keytra/releases) |
| **[keytra-action](https://github.com/keytra-app/keytra-action)** | Official GitHub Action to push source JSON, pull translations, and check progress in CI/CD | [GitHub Marketplace](https://github.com/marketplace/actions/keytra-i18n-sync) · [Releases](https://github.com/keytra-app/keytra-action/releases) |

### Why Keytra?

- **60-Second Self-Hosting:** Pre-built multi-arch Docker images (`linux/amd64`, `linux/arm64`) with automatic database migrations on startup.
- **Zero-SMTP Auth:** Guided `/setup` flow for the initial admin account and one-click invite links for translators.
- **JSON-First & Keyboard-Driven:** Nested and flat JSON, automatic `outdated` detection on source changes, placeholder variable validation, and `Cmd/Ctrl+Enter` save-and-next editing.
- **CI/CD Ready:** Scoped API keys (`ktr_`) and the official `keytra-app/keytra-action@v1` for automated sync and Pull Requests.

### Quick CI/CD Example

```yaml
- uses: keytra-app/keytra-action@v1
  with:
    url: [https://translate.example.com](https://translate.example.com)
    api-key: ${{ secrets.KEYTRA_API_KEY }}
    project: my-app
    mode: push
    source-path: locales/en/*.json

```

---

Questions, feedback, or self-hosting help? Start a thread in [Discussions](https://github.com/keytra-app/keytra/discussions). All projects are open-source under the **MIT License**.
