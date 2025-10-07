# Contributing to System Design Platform (Classic)

Thank you for wanting to contribute! This file outlines how to add content, services, and diagrams.

- Fork the repo and create a feature branch: `classic/<feature-name>`
- Keep each component in its own folder under `classic/system-design-platform/services/`.
- Use markdown for docs and include diagrams with Mermaid blocks.
- Tests: add unit tests under `tests/<service>/`.
- CI: add a lightweight GitHub Actions workflow that runs lint and tests for the changed service.

Pull request checklist:
- [ ] Title describes the change
- [ ] Updated README or related docs
- [ ] Unit tests added/updated
- [ ] CI workflow added/updated if service code is included

Maintainers will review and request changes or merge.
