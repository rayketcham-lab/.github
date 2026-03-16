# rayketcham-lab

Infrastructure-focused research lab. We build tooling at the intersection of enterprise PKI, cryptographic standards, and post-quantum migration.

---

## What We Do

We work on certificate authority infrastructure, cryptographic tooling, and security engineering — with a focus on real-world deployment at scale. Background spans enterprise CA management and Federal PKI operations, including experience with Federal Bridge cross-certification.

---

## Quantum Nexum

**[quantumnexum.com](https://quantumnexum.com)**

Post-quantum cryptography is no longer theoretical — NIST finalized ML-DSA, ML-KEM, and SLH-DSA in 2024. Most organizations aren't ready.

Quantum Nexum is a PQC PKI platform and educational resource built to close that gap. We document the standards, demonstrate real implementations, and build the infrastructure to prove they work at scale.

**SPORK CA** is the engine behind it — a Rust-based certificate authority with:
- ML-DSA and ML-KEM algorithm support
- - ACME protocol for automated certificate issuance
  - - A multi-tier CA hierarchy built for PQC from the ground up
   
    - Currently in active development and alpha testing. Watch this space.
   
    - ---

    ## Public Projects

    | Repo | Description |
    |------|-------------|
    | [parcl](https://github.com/rayketcham-lab/parcl) | Secure email certificate manager for Outlook — S/MIME encryption, signing, LDAP lookup |
    | [PKI-Client](https://github.com/rayketcham-lab/PKI-Client) | PKI operations CLI — certificate inspection, key management, TLS probing, enrollment protocols |
    | [PKI-Signing-Service](https://github.com/rayketcham-lab/PKI-Signing-Service) | Rust code signing engine — Authenticode, PKCS#7/CMS, RFC 3161 timestamping |
    | [issue-reporter](https://github.com/rayketcham-lab/issue-reporter) | Drop-in feedback widget — reports become GitHub issues, no backend, no dependencies |

    ---

    ## Stack

    Rust · C# · Python · ACME · X.509 · FIPS 140 · NIST PQC Standards

    ---

    *More coming as projects mature out of the lab.*
