# Contributing to Ketcham Lab Projects

Thanks for your interest in contributing. We welcome bug reports, feature requests, documentation improvements, and code contributions.

## Getting Started

1. **Check existing issues** — your problem or idea may already be tracked.
2. **Open an issue first** for non-trivial changes so we can discuss the approach before you invest time coding.
3. **Fork the repo** and create a feature branch from `main` (or `master`, depending on the repo).

## Development Standards

### Code Quality

- **Rust**: `cargo clippy -- -D warnings` (zero warnings), `cargo fmt` before committing
- **Python**: Python 3.12+, lint with `ruff`, type hints on public APIs
- **Shell**: `set -euo pipefail`, `shellcheck` clean, quote all variables
- **JavaScript**: No dependencies unless absolutely necessary

### Commits

We use [Conventional Commits](https://www.conventionalcommits.org/):

```
feat: add DANE TLSA record validation
fix: handle expired intermediate in chain builder
test: add adversarial input tests for cert parser
docs: update EST enrollment examples
```

### Pull Requests

- Keep PRs focused — one logical change per PR
- Include tests for new features and bug fixes
- Security-related code requires adversarial tests
- All CI checks must pass before merge

## Security Vulnerabilities

**Do not open a public issue for security vulnerabilities.** See [SECURITY.md](SECURITY.md) for responsible disclosure instructions.

## License

By contributing, you agree that your contributions will be licensed under the same license as the project you're contributing to.

## Questions?

Open a Discussion on the relevant repository, or email root@quantumnexum.com.
