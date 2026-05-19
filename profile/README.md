# rayketcham-lab

Infrastructure-focused research lab building at the intersection of enterprise PKI, post-quantum cryptography, and security engineering.

![Apache 2.0](https://img.shields.io/badge/license-Apache%202.0-blue)&nbsp;
![Repos](https://img.shields.io/badge/public%20repos-10-green)&nbsp;
![Commit Signing](https://img.shields.io/badge/commit%20signing-required-brightgreen)&nbsp;
![2FA](https://img.shields.io/badge/2FA-required-brightgreen)

---

## What We Do

Certificate authority infrastructure, cryptographic tooling, and security engineering — focused on real-world deployment at scale. Background spans enterprise CA management and Federal PKI operations, including Federal Bridge cross-certification.

On the consumer side we're building **HomePKI** — a private CA for the home network, delivered as a single static Linux binary with post-quantum algorithms available today.

We're also exploring AI-driven project ideation with **Project Forge**, an autonomous think-tank engine that generates, scores, and scaffolds security-focused project ideas.

---

## Quantum Nexum

> **[quantumnexum.com](https://quantumnexum.com)** &mdash; the flagship of this lab.
>
> Post-quantum cryptography is no longer theoretical &mdash; NIST finalized ML-DSA, ML-KEM, and SLH-DSA in 2024.  Most organizations aren't ready.  Quantum Nexum is a post-quantum PKI platform, software stack, and educational resource built to close that gap.

![PKI Coming Soon](https://img.shields.io/badge/PKI-Coming_Soon-yellow)&nbsp;
![Alpha](https://img.shields.io/badge/software-Alpha-red)&nbsp;
![ML-DSA](https://img.shields.io/badge/signatures-ML--DSA_(FIPS_204)-blueviolet)&nbsp;
![ACME Coming Soon](https://img.shields.io/badge/ACME-Coming_Soon-yellow)

### Status today

- **PKI** &mdash; coming soon, being refactored.  The previous post-quantum CA hierarchy is on hold; a clean rebuild around ML-DSA-87 (root) and ML-DSA-65 (policy + issuing) is in flight.  AIA, CRL, and OCSP endpoints at [pki.quantumnexum.com](https://pki.quantumnexum.com/) will return once the new hierarchy lands.
- **ACME** &mdash; coming soon, gated on the PKI refactor.  Will be an [RFC&nbsp;8555](https://datatracker.ietf.org/doc/html/rfc8555) endpoint at [acme.quantumnexum.com](https://acme.quantumnexum.com/) issuing post-quantum certs against the QN trust anchor.
- **Forge** &mdash; in development.  Hands-on PQ tooling: keygen, hybrid TLS, algorithm compare, OpenSSL 3.5 walkthroughs.  At [/forge/](https://quantumnexum.com/forge/).
- **Vault** &mdash; in development.  Reference library covering FIPS 203/204/205, the IETF LAMPS PQ RFCs, OpenSSL 3.5 LTS, liboqs 0.11.0+, and the CNSA&nbsp;2.0 / NSM-10 timelines.  At [/vault/](https://quantumnexum.com/vault/).

### Software (alpha)

- **Spork** &mdash; pure-Rust post-quantum certificate authority.  ML-DSA + SLH-DSA signing, ACME/EST/SCEP enrollment, OCSP, CRLs.  Will power the QN PKI once the refactor lands; self-hostable today against your own private trust anchor.  Single static binary, BSL 1.1.  Public site: [/spork/](https://quantumnexum.com/spork/).
- **Parcl** &mdash; S/MIME certificate manager and encryption add-in for Microsoft Outlook.  Native S/MIME, LDAP directory lookup, RFC 5751/7508 compliant.  Repo: [parcl](https://github.com/rayketcham-lab/parcl).
- **`spork-acme-installer`** &mdash; self-extracting installer for the standalone Spork ACME server.

### Education

Reference library, hands-on tools, and explainers covering NIST FIPS 203/204/205, the NSA CNSA&nbsp;2.0 timeline (NSS exclusive use by 2033) vs. NSM-10 (broader 2035 goal), the IETF LAMPS PQ RFC stack (RFCs 9881, 9882, 9909, 9814, 9935, 9936, 9763), and implementation guidance for OpenSSL 3.5 LTS and liboqs 0.11.0+.  All content stamped with `qn-last-verified` and CI-checked for drift.

[Visit quantumnexum.com →](https://quantumnexum.com)

---

## Spotlight

### HomePKI

Your own Certificate Authority for your home network. One static Linux binary (musl, x86_64 + aarch64), post-quantum ready today, no cloud, no account. Issue real TLS certificates for routers, NAS, cameras, Home Assistant, and any device on your LAN — signed by a CA that belongs to you alone.

![Pre-release](https://img.shields.io/badge/status-Pre--release-yellow)&nbsp;
![Rust](https://img.shields.io/badge/Rust-DEA584?logo=rust&logoColor=white)&nbsp;
![Post-quantum](https://img.shields.io/badge/post--quantum-ML--DSA_%2B_SLH--DSA-blueviolet)&nbsp;
![License](https://img.shields.io/github/license/rayketcham-lab/HomePKI)

[View Repository →](https://github.com/rayketcham-lab/HomePKI) &nbsp;|&nbsp; [FAQ →](https://github.com/rayketcham-lab/HomePKI/blob/main/docs/faq.md)

---

### PKI-Signing-Service

Pure Rust code signing engine supporting Authenticode (PE/CAB/MSI), PKCS#7/CMS, RFC 3161 timestamping, and PowerShell script signing. Multi-algorithm support including RSA, ECDSA, Ed25519, and **ML-DSA** (post-quantum). REST API for integration into CI/CD pipelines.

[![CI](https://github.com/rayketcham-lab/PKI-Signing-Service/workflows/CI/badge.svg)](https://github.com/rayketcham-lab/PKI-Signing-Service/actions)&nbsp;
![Alpha](https://img.shields.io/badge/status-Alpha-red)&nbsp;
![Rust](https://img.shields.io/badge/Rust-DEA584?logo=rust&logoColor=white)&nbsp;
![License](https://img.shields.io/github/license/rayketcham-lab/PKI-Signing-Service)

[View Repository →](https://github.com/rayketcham-lab/PKI-Signing-Service) &nbsp;|&nbsp; [API Docs →](https://rayketcham-lab.github.io/PKI-Signing-Service/)

---

### PKI-Client

Modern PKI operations tool for certificate inspection, key management, TLS probing, compliance validation, and DANE. Built as an `openssl` replacement for operators who need to debug and manage certificate infrastructure at scale.

[![CI](https://github.com/rayketcham-lab/PKI-Client/workflows/CI/badge.svg)](https://github.com/rayketcham-lab/PKI-Client/actions)&nbsp;
![Alpha](https://img.shields.io/badge/status-Alpha-red)&nbsp;
![Rust](https://img.shields.io/badge/Rust-DEA584?logo=rust&logoColor=white)&nbsp;
![License](https://img.shields.io/github/license/rayketcham-lab/PKI-Client)

[View Repository →](https://github.com/rayketcham-lab/PKI-Client) &nbsp;|&nbsp; [Docs →](https://rayketcham-lab.github.io/PKI-Client/)

---

### qn-claude-web

Self-hosted web frontend for Claude Code CLI — access Claude Code from any browser, any device, anywhere on your network. Zero external dependencies beyond Python and a running Claude Code instance.

[![CI](https://github.com/rayketcham-lab/qn-claude-web/workflows/CI/badge.svg)](https://github.com/rayketcham-lab/qn-claude-web/actions)&nbsp;
![Alpha](https://img.shields.io/badge/status-Alpha-red)&nbsp;
![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)&nbsp;
![License](https://img.shields.io/github/license/rayketcham-lab/qn-claude-web)

[View Repository →](https://github.com/rayketcham-lab/qn-claude-web)

---

## Projects

| Repo | What It Does | Status |
|------|-------------|--------|
| **[parcl](https://github.com/rayketcham-lab/parcl)** | S/MIME Certificate Manager & Encryption Add-in for Microsoft Outlook — encryption, signing, LDAP lookup, RFC 5751/7508 compliant | [![CI](https://github.com/rayketcham-lab/parcl/workflows/CI/badge.svg)](https://github.com/rayketcham-lab/parcl/actions) ![C#](https://img.shields.io/badge/C%23-239120?logo=csharp&logoColor=white) |
| **[project-forge](https://github.com/rayketcham-lab/project-forge)** | Autonomous IT project think-tank engine — generates, scores, synthesizes, and scaffolds project ideas into GitHub repos with CI/CD | [![CI](https://github.com/rayketcham-lab/project-forge/workflows/CI/badge.svg)](https://github.com/rayketcham-lab/project-forge/actions) ![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white) |
| **[issue-reporter](https://github.com/rayketcham-lab/issue-reporter)** | Drop a feedback button on any web page. Reports become GitHub issues. No backend required. No dependencies. One file. | ![Alpha](https://img.shields.io/badge/status-Alpha-red) ![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black) |
| **[gh-tracker](https://github.com/rayketcham-lab/gh-tracker)** | Self-hosted GitHub analytics dashboard — archives traffic, referrers, issues, and workflows before the 14-day API expiry | ![Alpha](https://img.shields.io/badge/status-Alpha-red) ![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white) ![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white) |
| **[shadowtrap](https://github.com/rayketcham-lab/shadowtrap)** | Multi-protocol network honeypot for threat intelligence and attack pattern analysis | ![Alpha](https://img.shields.io/badge/status-Alpha-red) ![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white) |

---

## Security

We take security seriously across all projects:

- **Signed commits required** — all commits must have verified signatures
- **2FA enforced** — all org members
- **Dependency scanning** — Dependabot enabled across all repositories
- **Code scanning** — CodeQL and custom security workflows
- **Responsible disclosure** — see our [Security Policy](https://github.com/rayketcham-lab/.github/blob/main/SECURITY.md)

Found a vulnerability? Email **root@quantumnexum.com** or use GitHub's [private vulnerability reporting](https://docs.github.com/en/code-security/security-advisories/guidance-on-reporting-and-writing-information-about-vulnerabilities/privately-reporting-a-security-vulnerability).

---

## Stack

![Rust](https://img.shields.io/badge/Rust-DEA584?style=for-the-badge&logo=rust&logoColor=white)&nbsp;
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)&nbsp;
![C#](https://img.shields.io/badge/C%23-239120?style=for-the-badge&logo=csharp&logoColor=white)&nbsp;
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)&nbsp;
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)&nbsp;
![Godot](https://img.shields.io/badge/Godot-478CBF?style=for-the-badge&logo=godotengine&logoColor=white)

---

## Contributing

We build in the open where we can. Contributions, issues, and discussions are welcome on any of our public repositories.

- Read our [Contributing Guide](https://github.com/rayketcham-lab/.github/blob/main/CONTRIBUTING.md)
- Review our [Code of Conduct](https://github.com/rayketcham-lab/.github/blob/main/CODE_OF_CONDUCT.md)
- Open a [Discussion](https://github.com/orgs/rayketcham-lab/discussions) on any repo

---

## Get In Touch

**Web** &mdash; [quantumnexum.com](https://quantumnexum.com) &nbsp;|&nbsp; **Email** &mdash; root@quantumnexum.com

---

*Building in the open.*
