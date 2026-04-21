# Contributing

## Before You Start

- Check existing issues first.
- Open an issue before writing code for non-trivial changes. Don't waste your time building something we won't merge.
- Fork the repo, branch from `main` (or `master`).

## Standards

**Your code must:**

- Pass CI — zero warnings, zero lint failures
- Include tests for new features and bug fixes
- Use conventional commits: `feat:`, `fix:`, `test:`, `docs:`, `security:`, `refactor:`

**Language-specific:**

| Language | Lint | Format | Notes |
|----------|------|--------|-------|
| Rust | `cargo clippy -- -D warnings` | `cargo fmt` | No hand-rolled crypto |
| Python | `ruff check` | `ruff format` | 3.12+, type hints on public APIs |
| Shell | `shellcheck` | — | `set -euo pipefail`, quote everything |
| C# | Roslyn analyzers | — | Follow existing project style |

## Pull Requests

- One logical change per PR. Don't bundle unrelated work.
- Security code requires adversarial tests.
- All CI checks pass before review.

## Security Vulnerabilities

**Do not open a public issue.** See [SECURITY.md](SECURITY.md).

## License

Your contributions are licensed under the same license as the project.
