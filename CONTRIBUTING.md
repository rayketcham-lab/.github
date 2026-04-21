# Contributing

This guide covers the basics for contributing to any repository in the rayketcham-lab organization.

## Development Setup

### Prerequisites

Most projects use one of:

- **Rust** — stable toolchain via [rustup](https://rustup.rs/)
- **Python 3.12+** — with [uv](https://docs.astral.sh/uv/) (recommended) or pip
- **C# / .NET** — .NET 8.0+ SDK
- **JavaScript** — no build tools required (vanilla JS)

### Quick Start

```bash
git clone https://github.com/rayketcham-lab/<repo>.git
cd <repo>
```

Then follow the repo's own README for build/run instructions.

## Before Submitting

### Rust Projects

```bash
cargo fmt --all --check
cargo clippy --all-targets -- -D warnings
cargo test --all
```

### Python Projects

```bash
ruff check .
ruff format --check .
python -m pytest -v
```

### Shell Scripts

```bash
shellcheck <script>.sh
```

All checks must pass with zero warnings.

## Commit Messages

Follow [Conventional Commits](https://www.conventionalcommits.org/):

```
feat: add DANE TLSA record validation
fix: handle expired intermediate in chain builder
test: add adversarial input tests for cert parser
security: patch timing side-channel in signature verification
docs: update EST enrollment examples
refactor: extract timestamp client into module
ci: add MSRV check to pipeline
```

One logical change per commit.

## Pull Requests

1. Fork the repo and branch from `main` (or `master`).
2. Open an issue first for non-trivial changes.
3. Keep PRs focused — one logical change per PR.
4. Include tests for new features and bug fixes.
5. Security-critical code requires adversarial tests.
6. All CI checks must pass before review.

## Code Standards

- **No warnings** — zero-warning policy across all languages
- **No hand-rolled crypto** — use vetted libraries (`ring`, `rustls`, `aws-lc-rs`, RustCrypto, `openssl`)
- **Error handling mandatory** — no silent failures, no bare `except`
- **Input validation** at all trust boundaries
- **No secrets in code** — ever

## Security Vulnerabilities

**Do not open a public issue.** See [SECURITY.md](SECURITY.md) for disclosure instructions.

## License

Contributions are licensed under the same license as the project (Apache-2.0 for most repos).
