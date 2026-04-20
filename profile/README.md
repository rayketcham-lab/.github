# rayketcham-lab

Infrastructure-focused research lab building at the intersection of enterprise PKI, post-quantum cryptography, and security engineering.

![Apache 2.0](https://img.shields.io/badge/license-Apache%202.0-blue)&nbsp;
![Repos](https://img.shields.io/badge/public%20repos-7-green)&nbsp;
![Commit Signing](https://img.shields.io/badge/commit%20signing-required-brightgreen)&nbsp;
![2FA](https://img.shields.io/badge/2FA-required-brightgreen)

---

## What We Do

Certificate authority infrastructure, cryptographic tooling, and security engineering — focused on real-world deployment at scale. Background spans enterprise CA management and Federal PKI operations, including Federal Bridge cross-certification.

We're also exploring AI-driven project ideation with **Project Forge**, an autonomous think-tank engine that generates, scores, and scaffolds security-focused project ideas.

---

## Quantum Nexum

> **[quantumnexum.com](https://quantumnexum.com)**
>
> Post-quantum cryptography is no longer theoretical — NIST finalized ML-DSA, ML-KEM, and SLH-DSA in 2024. Most organizations aren't ready.
>
> Quantum Nexum is a PQC PKI platform and educational resource built to close that gap. We document the standards, demonstrate real implementations, and build the infrastructure to prove they work at scale.

---

## Spotlight

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
