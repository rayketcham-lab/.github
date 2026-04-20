# Security Policy

## Supported Versions

We provide security updates for the latest release of each project. Older versions are not supported.

## Reporting a Vulnerability

**Do not open a public GitHub issue for security vulnerabilities.**

Instead, please report vulnerabilities via one of these channels:

- **Email**: root@quantumnexum.com
- **GitHub**: Use the [private vulnerability reporting](https://docs.github.com/en/code-security/security-advisories/guidance-on-reporting-and-writing-information-about-vulnerabilities/privately-reporting-a-security-vulnerability) feature on the affected repository (if enabled)

### What to Include

- Description of the vulnerability
- Steps to reproduce
- Affected version(s)
- Impact assessment (if known)
- Suggested fix (if any)

### What to Expect

- **Acknowledgment** within 48 hours
- **Initial assessment** within 7 days
- **Fix or mitigation** timeline communicated after assessment
- **Credit** in the security advisory (unless you prefer to remain anonymous)

## Scope

This policy applies to all repositories in the [rayketcham-lab](https://github.com/rayketcham-lab) organization.

### In Scope

- Authentication and authorization flaws
- Cryptographic implementation issues
- Injection vulnerabilities (command, SQL, XSS, etc.)
- Certificate validation bypasses
- Private key exposure
- SSRF and path traversal

### Out of Scope

- Denial of service (unless it affects availability of PKI services)
- Social engineering
- Issues in third-party dependencies (report upstream, but let us know)

## Cryptographic Standards

Our PKI projects follow these standards:

- No hand-rolled cryptography — we use `ring`, `rustls`, or `openssl`
- FIPS 140-3 compliance where applicable
- Post-quantum algorithm support (ML-DSA, ML-KEM, SLH-DSA) per NIST FIPS 203/204/205
