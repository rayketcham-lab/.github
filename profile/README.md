<div align="center">

# 🔐 Ketcham Lab

### Enterprise PKI · Post-Quantum Cryptography · Security Engineering

Home of **[Quantum Nexum](https://quantumnexum.com)** — a post-quantum PKI platform, software stack, and educational resource built for the real world.

[![Website](https://img.shields.io/badge/quantumnexum.com-6f42c1)](https://quantumnexum.com)
[![Post-Quantum](https://img.shields.io/badge/post--quantum-ML--DSA%20%2B%20SLH--DSA-8a2be2)](https://quantumnexum.com)
[![Signed commits required](https://img.shields.io/badge/commits-signed%20%26%20verified-2ea44f?logo=github&logoColor=white)](https://github.com/rayketcham-lab/.github/blob/main/SECURITY.md)
[![2FA required](https://img.shields.io/badge/2FA-required-2ea44f?logo=github&logoColor=white)](https://github.com/rayketcham-lab/.github/blob/main/SECURITY.md)

</div>

---

## What We Do

We build certificate-authority infrastructure, cryptographic tooling, and security software — with an emphasis on real-world deployment and the migration to post-quantum cryptography. Background spans enterprise CA management and Federal PKI operations, including Federal Bridge cross-certification.

Our flagship is **Quantum Nexum**, a post-quantum PKI platform. Alongside it we ship open tooling for PKI operators and developers, and we're building **HomePKI** — a private certificate authority for the home network (currently in private beta).

---

## 🌌 Quantum Nexum &mdash; flagship

> **[quantumnexum.com](https://quantumnexum.com)**
>
> Post-quantum cryptography is no longer theoretical &mdash; NIST finalized ML-DSA, ML-KEM, and SLH-DSA (FIPS&nbsp;203/204/205) in 2024. Most organizations aren't ready. Quantum Nexum is a post-quantum PKI platform, software stack, and educational resource built to close that gap.

![PKI Coming Soon](https://img.shields.io/badge/PKI-coming_soon-yellow)&nbsp;
![Alpha](https://img.shields.io/badge/software-alpha-red)&nbsp;
![ML-DSA](https://img.shields.io/badge/signatures-ML--DSA_(FIPS_204)-8a2be2)&nbsp;
![ACME Coming Soon](https://img.shields.io/badge/ACME-coming_soon-yellow)

<details>
<summary><b>Platform status</b> &mdash; what's live and what's in flight</summary>

<br>

- **PKI** &mdash; being rebuilt around ML-DSA-87 (root) and ML-DSA-65 (policy + issuing). AIA, CRL, and OCSP endpoints at [pki.quantumnexum.com](https://pki.quantumnexum.com/) return once the new hierarchy lands.
- **ACME** &mdash; an [RFC&nbsp;8555](https://datatracker.ietf.org/doc/html/rfc8555) endpoint at [acme.quantumnexum.com](https://acme.quantumnexum.com/), gated on the PKI rebuild, issuing post-quantum certs against the QN trust anchor.
- **Forge** &mdash; hands-on PQ tooling: keygen, signatures, hybrid TLS, algorithm compare, OpenSSL 3.5 walkthroughs, cert inspector, migration decision tree, signature-size calculator. At [/forge/](https://quantumnexum.com/forge/).
- **Vault** &mdash; reference library covering FIPS 203/204/205, the IETF LAMPS PQ RFCs, OpenSSL 3.5 LTS, liboqs, and the CNSA&nbsp;2.0 / NSM-10 timelines. At [/vault/](https://quantumnexum.com/vault/).

</details>

**Platform software** (private beta &mdash; follow [quantumnexum.com](https://quantumnexum.com) for availability):

- **Spork** &mdash; pure-Rust post-quantum certificate authority. ML-DSA + SLH-DSA signing, ACME/EST/SCEP enrollment, OCSP, CRLs. Single static binary, BSL&nbsp;1.1. Public site: [/spork/](https://quantumnexum.com/spork/).
- **HomePKI** &mdash; your own CA for the home network: one static Linux binary, post-quantum ready, no cloud, no account. Issue real TLS certificates for routers, NAS, cameras, and Home Assistant &mdash; signed by a CA that belongs to you alone.

---

## 📦 Public Showcase

Open code you can use today. Every status badge below is **live** &mdash; release, CI, and license read straight from each repository, so they never go stale.

### 🔐 PKI &amp; Post-Quantum Crypto

| Project | What it does | Status |
|---------|--------------|--------|
| **[PKI-Client](https://github.com/rayketcham-lab/PKI-Client)** · [docs](https://rayketcham-lab.github.io/PKI-Client/) | Pure-Rust PKI CLI &mdash; inspect certificates, generate keys, probe TLS, validate FIPS 140-3 / NIST SP 800-57 / Federal Bridge compliance, and build CA hierarchies. No OpenSSL; one static musl binary. Opt-in post-quantum (ML-DSA, SLH-DSA) via `--features pqc`. | [![release](https://img.shields.io/github/v/release/rayketcham-lab/PKI-Client?label=release&color=2ea44f)](https://github.com/rayketcham-lab/PKI-Client/releases) [![CI](https://img.shields.io/github/actions/workflow/status/rayketcham-lab/PKI-Client/ci.yml?branch=main&label=CI)](https://github.com/rayketcham-lab/PKI-Client/actions) [![license](https://img.shields.io/github/license/rayketcham-lab/PKI-Client?color=blue)](https://github.com/rayketcham-lab/PKI-Client/blob/main/LICENSE) |
| **[PKI-Signing-Service](https://github.com/rayketcham-lab/PKI-Signing-Service)** · [docs](https://rayketcham-lab.github.io/PKI-Signing-Service/) | Pure-Rust code-signing engine &mdash; Authenticode (PE/CAB/MSI), PKCS#7/CMS, RFC 3161 timestamping, PowerShell SIP, detached CMS. Runs as CLI, REST API, or a standalone TSA server; batch signing and PFX import. ML-DSA opt-in via `--features pq-experimental`. | [![release](https://img.shields.io/github/v/release/rayketcham-lab/PKI-Signing-Service?label=release&color=2ea44f)](https://github.com/rayketcham-lab/PKI-Signing-Service/releases) [![CI](https://img.shields.io/github/actions/workflow/status/rayketcham-lab/PKI-Signing-Service/ci.yml?branch=main&label=CI)](https://github.com/rayketcham-lab/PKI-Signing-Service/actions) [![license](https://img.shields.io/github/license/rayketcham-lab/PKI-Signing-Service?color=blue)](https://github.com/rayketcham-lab/PKI-Signing-Service/blob/main/LICENSE) |
| **[parcl](https://github.com/rayketcham-lab/parcl)** | S/MIME encryption, signing, and certificate management add-in for Microsoft Outlook &mdash; LDAP directory lookup, AES-256, RFC 5751/7508 compliant. **⚠️ Under active rework &mdash; releases pulled; not for install yet.** | [![license](https://img.shields.io/github/license/rayketcham-lab/parcl?color=blue)](https://github.com/rayketcham-lab/parcl/blob/main/LICENSE) [![status](https://img.shields.io/badge/status-rework-orange)](https://github.com/rayketcham-lab/parcl) |

### 🛡️ Security Tooling

| Project | What it does | Status |
|---------|--------------|--------|
| **[shadowtrap](https://github.com/rayketcham-lab/shadowtrap)** | Multi-protocol network honeypot &mdash; 21 emulated services (SSH, HTTP, MySQL, Redis, RDP, SMB, and more), honeytokens that fire on access, full payload capture with GeoIP and threat scoring, and a real-time HTTPS dashboard. | [![CI](https://img.shields.io/github/actions/workflow/status/rayketcham-lab/shadowtrap/ci.yml?branch=main&label=CI)](https://github.com/rayketcham-lab/shadowtrap/actions) [![license](https://img.shields.io/github/license/rayketcham-lab/shadowtrap?color=blue)](https://github.com/rayketcham-lab/shadowtrap/blob/main/LICENSE) |

### 🧰 Developer Tooling

| Project | What it does | Status |
|---------|--------------|--------|
| **[qn-claude-web](https://github.com/rayketcham-lab/qn-claude-web)** | Self-hosted web UI for the Claude Code CLI &mdash; full xterm.js terminal, persistent tmux sessions, chat, and multi-agent orchestration from any browser or device on your network. Pure Python, no build step. | [![release](https://img.shields.io/github/v/release/rayketcham-lab/qn-claude-web?label=release&color=2ea44f)](https://github.com/rayketcham-lab/qn-claude-web/releases) [![CI](https://img.shields.io/github/actions/workflow/status/rayketcham-lab/qn-claude-web/ci.yml?branch=main&label=CI)](https://github.com/rayketcham-lab/qn-claude-web/actions) [![license](https://img.shields.io/github/license/rayketcham-lab/qn-claude-web?color=blue)](https://github.com/rayketcham-lab/qn-claude-web/blob/main/LICENSE) |
| **[issue-reporter](https://github.com/rayketcham-lab/issue-reporter)** | Drop a feedback button on any web page &mdash; reports become GitHub issues. One file, zero dependencies, no backend. Auto-captures console errors, recent API calls, and DOM context; strict CSP and SRI supply-chain pinning. | [![release](https://img.shields.io/github/v/release/rayketcham-lab/issue-reporter?label=release&color=2ea44f)](https://github.com/rayketcham-lab/issue-reporter/releases) [![CodeQL](https://img.shields.io/github/actions/workflow/status/rayketcham-lab/issue-reporter/codeql.yml?branch=main&label=CodeQL)](https://github.com/rayketcham-lab/issue-reporter/actions) [![license](https://img.shields.io/github/license/rayketcham-lab/issue-reporter?color=blue)](https://github.com/rayketcham-lab/issue-reporter/blob/main/LICENSE) |
| **[project-forge](https://github.com/rayketcham-lab/project-forge)** | Autonomous idea-generation engine &mdash; scores every idea on feasibility, fundability, and ambition across 19 categories, then human-gates one-click promotion to GitHub issues. FastAPI + SQLite; ~$2&ndash;3/mo on Haiku 4.5 (or free via the Claude Code CLI). | [![CI](https://img.shields.io/github/actions/workflow/status/rayketcham-lab/project-forge/ci.yml?branch=main&label=CI)](https://github.com/rayketcham-lab/project-forge/actions) [![license](https://img.shields.io/github/license/rayketcham-lab/project-forge?color=lightgrey)](https://github.com/rayketcham-lab/project-forge) |
| **[gh-tracker](https://github.com/rayketcham-lab/gh-tracker)** | Self-hosted GitHub analytics dashboard &mdash; archives traffic, referrers, people, issues, and self-hosted runner state to SQLite before GitHub's 14-day API wipe. FastAPI backend, React dashboard. | [![release](https://img.shields.io/github/v/release/rayketcham-lab/gh-tracker?label=release&color=2ea44f)](https://github.com/rayketcham-lab/gh-tracker/releases) [![CI](https://img.shields.io/github/actions/workflow/status/rayketcham-lab/gh-tracker/ci.yml?branch=main&label=CI)](https://github.com/rayketcham-lab/gh-tracker/actions) [![license](https://img.shields.io/github/license/rayketcham-lab/gh-tracker?color=lightgrey)](https://github.com/rayketcham-lab/gh-tracker) |

> Licensing varies by project &mdash; each badge above reflects that repository's own `LICENSE`. Most tooling is Apache-2.0; shadowtrap is MIT. A couple of early-stage repos aren't licensed for reuse yet (the badge will say so).

---

## 🔒 Security &amp; Trust

We take security seriously across all repositories:

- **Signed commits required** &mdash; every commit must carry a verified signature
- **2FA enforced** &mdash; for all organization members
- **Dependency scanning** &mdash; Dependabot enabled across repositories
- **Code scanning** &mdash; CodeQL and custom security workflows
- **Responsible disclosure** &mdash; see our [Security Policy](https://github.com/rayketcham-lab/.github/blob/main/SECURITY.md)

Found a vulnerability? Email **root@quantumnexum.com** or use GitHub's [private vulnerability reporting](https://docs.github.com/en/code-security/security-advisories/guidance-on-reporting-and-writing-information-about-vulnerabilities/privately-reporting-a-security-vulnerability).

---

## 🛠️ Tech Stack

![Rust](https://img.shields.io/badge/Rust-DEA584?style=for-the-badge&logo=rust&logoColor=black)&nbsp;
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)&nbsp;
![C#](https://img.shields.io/badge/C%23-239120?style=for-the-badge&logo=csharp&logoColor=white)&nbsp;
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)

---

## 🤝 Contributing

We build in the open where we can. Contributions and issues are welcome on any of our public repositories.

- Read our [Contributing Guide](https://github.com/rayketcham-lab/.github/blob/main/CONTRIBUTING.md)
- Review our [Code of Conduct](https://github.com/rayketcham-lab/.github/blob/main/CODE_OF_CONDUCT.md)
- Spot something? Open an issue on the relevant repository above

---

## 📫 Get In Touch

**Web** &mdash; [quantumnexum.com](https://quantumnexum.com) &nbsp;|&nbsp; **Email** &mdash; root@quantumnexum.com

---

<div align="center"><sub><i>Building in the open.</i></sub></div>
