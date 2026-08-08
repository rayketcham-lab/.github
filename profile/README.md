<div align="center">

<img src="https://raw.githubusercontent.com/rayketcham-lab/.github/main/profile/assets/banner.svg" alt="Ketcham Lab — post-quantum PKI, cryptographic tooling, security engineering" width="100%">

<br><br>

Home of **[Quantum Nexum](https://quantumnexum.com)** — post-quantum trust infrastructure: a certificate-authority program, a software stack, and an engineering resource built for the real world.

[![Website](https://img.shields.io/badge/quantumnexum.com-live-3DDC97?labelColor=0E1114)](https://quantumnexum.com)
[![Post-Quantum](https://img.shields.io/badge/post--quantum-ML--DSA%20%2B%20SLH--DSA-8957e5?labelColor=0E1114)](https://csrc.nist.gov/pubs/fips/204/final)
[![Actions SHA-pinned](https://img.shields.io/badge/actions-SHA--pinned-2ea44f?logo=github&logoColor=white)](https://github.com/rayketcham-lab/.github/blob/main/SECURITY.md)
[![2FA required](https://img.shields.io/badge/2FA-required-2ea44f?logo=github&logoColor=white)](https://github.com/rayketcham-lab/.github/blob/main/SECURITY.md)

</div>

---

## What We Do

We build certificate-authority infrastructure, cryptographic tooling, and security software — with an emphasis on real-world deployment and the migration to post-quantum cryptography.  Background spans enterprise CA management and Federal PKI operations, including Federal Bridge cross-certification.

Our flagship is **Quantum Nexum**.  Alongside it we ship open tooling for PKI operators and developers, and we're building **HomePKI** — a private certificate authority for the home network (currently in private beta).

---

## 🌌 Quantum Nexum — flagship

> **[quantumnexum.com](https://quantumnexum.com)**
>
> Post-quantum cryptography is no longer theoretical — NIST finalized ML-DSA, ML-KEM, and SLH-DSA (FIPS 203/204/205) in 2024.  Most organizations aren't ready.  Quantum Nexum is post-quantum trust infrastructure built to close that gap — redesigned and relaunched June 2026.

![Site live](https://img.shields.io/badge/site-live-3DDC97?labelColor=0E1114)&nbsp;
![PKI rebuild](https://img.shields.io/badge/PKI-rebuild_in_progress-E5B567?labelColor=0E1114)&nbsp;
![ACME planned](https://img.shields.io/badge/ACME-planned-yellow?labelColor=0E1114)&nbsp;
![Software alpha](https://img.shields.io/badge/software-alpha-E5736B?labelColor=0E1114)&nbsp;
![ML-DSA](https://img.shields.io/badge/signatures-ML--DSA_(FIPS_204)-8957e5?labelColor=0E1114)

<details>
<summary><b>Platform status</b> — what's live and what's in flight</summary>

<br>

- **PKI** — a 22-CA ML-DSA hierarchy (ML-DSA-87 root; ML-DSA-65 policy + issuing across seven policy branches), currently being rebuilt.  The landing at [pki.quantumnexum.com](https://pki.quantumnexum.com/) is live; AIA, CRL, and OCSP publication return as the new chain lands.  Design: [/pki/](https://quantumnexum.com/pki/).
- **ACME** — an [RFC 8555](https://datatracker.ietf.org/doc/html/rfc8555) directory at [acme.quantumnexum.com](https://acme.quantumnexum.com/), issuing post-quantum certs against the QN trust anchor.  Landing live; the directory opens once the PKI rebuild lands.  Details: [/acme/](https://quantumnexum.com/acme/).
- **Forge** — hands-on PQ tooling, live and growing: keygen, signatures, algorithm compare, OpenSSL 3.5 recipes.  At [/forge/](https://quantumnexum.com/forge/).
- **Vault** — reference library, live and growing: FIPS 203/204/205, the IETF LAMPS PQ RFCs, OpenSSL 3.5 LTS, liboqs, and the CNSA 2.0 / NSM-10 timelines.  At [/vault/](https://quantumnexum.com/vault/).

</details>

**Platform software** (alpha — early builds on request via [quantumnexum.com](https://quantumnexum.com)):

- **Spork** — post-quantum certificate authority written in Rust.  ML-DSA + SLH-DSA alongside classical ECDSA/RSA/Ed25519; ACME, EST, and SCEP enrollment; OCSP and CRLs.  Single static binary (Linux x86_64), RustCrypto primitives — no OpenSSL dependency.  BSL 1.1.  Public site: [/spork/](https://quantumnexum.com/spork/).
- **HomePKI** — your own CA for the home network: one static Linux binary, post-quantum ready, no cloud, no account.  Issue real TLS certificates for routers, NAS, cameras, and Home Assistant — signed by a CA that belongs to you alone.  Private beta.

---

## 📡 Now — August 2026

- **Supply-chain hardening across the org** — every GitHub Actions workflow in every active repository is now pinned to a commit SHA rather than a floating tag, enforced org-wide by policy
- **tailnumber** published its [public overview](https://github.com/rayketcham-lab/tailnumber) — the design writeup stays open; the evaluation demo has been retired and the implementation remains private
- **QN PKI** hierarchy rebuild underway — AIA/CRL/OCSP publication and the ACME directory follow it

---

## 📦 Public Showcase

Open code you can use today.  Release, CI, and license badges read straight from each repository, so they never go stale.

### 🔐 PKI & Post-Quantum Crypto

| Project | What it does | Status |
|---------|--------------|--------|
| **[tailnumber](https://github.com/rayketcham-lab/tailnumber)** | Detached Hash-Signing as a Service (dHSaaS) — send a hash, get back a portable signed proof.  ML-DSA and hybrid classical+PQ signatures, HSM-held non-extractable keys, 50-year trust chain, offline verification with nothing but OpenSSL.  The [design writeup](https://github.com/rayketcham-lab/tailnumber) is public — key rotation, generational CAs, and why rotation alone doesn't keep a decades-old signature verifiable.  Implementation private; evaluation demo retired. | [![demo](https://img.shields.io/badge/demo-retired-6e7781)](https://github.com/rayketcham-lab/tailnumber) [![source](https://img.shields.io/badge/source-private-lightgrey)](https://github.com/rayketcham-lab/tailnumber) |
| **[PKI-Client](https://github.com/rayketcham-lab/PKI-Client)** · [docs](https://rayketcham-lab.github.io/PKI-Client/) | Pure-Rust PKI CLI — inspect certificates, generate keys, probe TLS, validate FIPS 140-3 / NIST SP 800-57 / Federal Bridge compliance, and build CA hierarchies.  No OpenSSL; one static musl binary.  Opt-in post-quantum (ML-DSA, SLH-DSA) via `--features pqc`. | [![release](https://img.shields.io/github/v/release/rayketcham-lab/PKI-Client?label=release&color=2ea44f)](https://github.com/rayketcham-lab/PKI-Client/releases) [![CI](https://img.shields.io/github/actions/workflow/status/rayketcham-lab/PKI-Client/ci.yml?branch=main&label=CI)](https://github.com/rayketcham-lab/PKI-Client/actions) [![license](https://img.shields.io/github/license/rayketcham-lab/PKI-Client?color=blue)](https://github.com/rayketcham-lab/PKI-Client/blob/main/LICENSE) |
| **[PKI-Signing-Service](https://github.com/rayketcham-lab/PKI-Signing-Service)** · [docs](https://rayketcham-lab.github.io/PKI-Signing-Service/) | Pure-Rust code-signing engine — Authenticode (PE/CAB/MSI), PKCS#7/CMS, RFC 3161 timestamping, PowerShell SIP, detached CMS.  Runs as CLI, REST API, or a standalone TSA server; batch signing and PFX import.  ML-DSA opt-in via `--features pq-experimental`. | [![release](https://img.shields.io/github/v/release/rayketcham-lab/PKI-Signing-Service?label=release&color=2ea44f)](https://github.com/rayketcham-lab/PKI-Signing-Service/releases) [![CI](https://img.shields.io/github/actions/workflow/status/rayketcham-lab/PKI-Signing-Service/ci.yml?branch=main&label=CI)](https://github.com/rayketcham-lab/PKI-Signing-Service/actions) [![license](https://img.shields.io/github/license/rayketcham-lab/PKI-Signing-Service?color=blue)](https://github.com/rayketcham-lab/PKI-Signing-Service/blob/main/LICENSE) |
| **[parcl](https://github.com/rayketcham-lab/parcl)** | S/MIME encryption, signing, and certificate management add-in for Microsoft Outlook — LDAP directory lookup, AES-256, RFC 5751/7508 compliant.  **⚠️ Under active rework — releases pulled; not for install yet.** | [![license](https://img.shields.io/github/license/rayketcham-lab/parcl?color=blue)](https://github.com/rayketcham-lab/parcl/blob/main/LICENSE) [![status](https://img.shields.io/badge/status-rework-orange)](https://github.com/rayketcham-lab/parcl) |

### 🧰 Developer Tooling

| Project | What it does | Status |
|---------|--------------|--------|
| **[qn-claude-web](https://github.com/rayketcham-lab/qn-claude-web)** | Self-hosted web UI for the Claude Code CLI — full xterm.js terminal, persistent tmux sessions, chat, and multi-agent orchestration from any browser or device on your network.  Pure Python, no build step. | [![release](https://img.shields.io/github/v/release/rayketcham-lab/qn-claude-web?label=release&color=2ea44f)](https://github.com/rayketcham-lab/qn-claude-web/releases) [![CI](https://img.shields.io/github/actions/workflow/status/rayketcham-lab/qn-claude-web/ci.yml?branch=main&label=CI)](https://github.com/rayketcham-lab/qn-claude-web/actions) [![license](https://img.shields.io/github/license/rayketcham-lab/qn-claude-web?color=blue)](https://github.com/rayketcham-lab/qn-claude-web/blob/main/LICENSE) |
| **[issue-reporter](https://github.com/rayketcham-lab/issue-reporter)** | Drop a feedback button on any web page — reports become GitHub issues.  One file, zero dependencies, no backend.  Auto-captures console errors, recent API calls, and DOM context; strict CSP and SRI supply-chain pinning. | [![release](https://img.shields.io/github/v/release/rayketcham-lab/issue-reporter?label=release&color=2ea44f)](https://github.com/rayketcham-lab/issue-reporter/releases) [![CodeQL](https://img.shields.io/github/actions/workflow/status/rayketcham-lab/issue-reporter/codeql.yml?branch=main&label=CodeQL)](https://github.com/rayketcham-lab/issue-reporter/actions) [![license](https://img.shields.io/github/license/rayketcham-lab/issue-reporter?color=blue)](https://github.com/rayketcham-lab/issue-reporter/blob/main/LICENSE) |
| **[project-forge](https://github.com/rayketcham-lab/project-forge)** | Autonomous idea-generation engine — scores every idea on feasibility, fundability, and ambition across 19 categories, then human-gates one-click promotion to GitHub issues.  FastAPI + SQLite; ~$2–3/mo on Haiku 4.5 (or free via the Claude Code CLI). | [![CI](https://img.shields.io/github/actions/workflow/status/rayketcham-lab/project-forge/ci.yml?branch=main&label=CI)](https://github.com/rayketcham-lab/project-forge/actions) [![license](https://img.shields.io/github/license/rayketcham-lab/project-forge?color=blue)](https://github.com/rayketcham-lab/project-forge/blob/main/LICENSE) |
| **[gh-tracker](https://github.com/rayketcham-lab/gh-tracker)** | Self-hosted GitHub analytics dashboard — archives traffic, referrers, people, issues, and self-hosted runner state to SQLite before GitHub's 14-day API wipe.  FastAPI backend, React dashboard. | [![release](https://img.shields.io/github/v/release/rayketcham-lab/gh-tracker?label=release&color=2ea44f)](https://github.com/rayketcham-lab/gh-tracker/releases) [![CI](https://img.shields.io/github/actions/workflow/status/rayketcham-lab/gh-tracker/ci.yml?branch=main&label=CI)](https://github.com/rayketcham-lab/gh-tracker/actions) [![license](https://img.shields.io/github/license/rayketcham-lab/gh-tracker?color=lightgrey)](https://github.com/rayketcham-lab/gh-tracker) |

> Licensing varies by project — each badge above reflects that repository's own `LICENSE`.  Most tooling is Apache-2.0; project-forge is MIT; tailnumber is proprietary (overview published, source closed).  gh-tracker isn't licensed for reuse yet, and its badge says so.

---

## 🔒 Security & Trust

We take security seriously across all repositories:

- **Branch rulesets** — every default branch blocks deletion, force-push, and non-linear history, and carries a commit-signature requirement
- **Pinned actions** — every workflow across every active repository references its GitHub Actions by commit SHA, not by mutable tag, enforced by org policy
- **Allow-listed actions** — workflows may only use GitHub-owned, verified, or explicitly approved publishers
- **2FA enforced** — for all organization members
- **Dependency scanning** — Dependabot enabled across repositories
- **Code scanning** — CodeQL and custom security workflows
- **Responsible disclosure** — see our [Security Policy](https://github.com/rayketcham-lab/.github/blob/main/SECURITY.md)

Found a vulnerability?  Email **root@quantumnexum.com** or use GitHub's [private vulnerability reporting](https://docs.github.com/en/code-security/security-advisories/guidance-on-reporting-and-writing-information-about-vulnerabilities/privately-reporting-a-security-vulnerability).

---

## 🛠️ Tech Stack

![Rust](https://img.shields.io/badge/Rust-DEA584?style=for-the-badge&logo=rust&logoColor=black)&nbsp;
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)&nbsp;
![C#](https://img.shields.io/badge/C%23-239120?style=for-the-badge&logo=csharp&logoColor=white)&nbsp;
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)

---

## 🤝 Contributing

We build in the open where we can.  Contributions and issues are welcome on any of our public repositories.

- Read our [Contributing Guide](https://github.com/rayketcham-lab/.github/blob/main/CONTRIBUTING.md)
- Review our [Code of Conduct](https://github.com/rayketcham-lab/.github/blob/main/CODE_OF_CONDUCT.md)
- Spot something?  Open an issue on the relevant repository above

---

## 📫 Get In Touch

**Web** — [quantumnexum.com](https://quantumnexum.com) &nbsp;|&nbsp; **Email** — root@quantumnexum.com

---

<div align="center"><sub><i>Building in the open.</i></sub></div>
