# Bonafide™

**Privacy by architecture, not by promise.**

Bonafide is an open specification for user-sovereign encrypted data vaults. Every piece of personal data is independently encrypted, keyed to the individual's biometric, and distributed across institutions that can see only what the user authorizes. There are no passwords. No recovery phrases. No master keys. No central authority that can be compelled to decrypt.

Institutions don't protect your data behind their walls — they host encrypted fragments they cannot read.

---

## The Problem

Every major breach shares the same root cause: centralized databases full of plaintext personal data, protected by perimeter security that eventually fails. Users bear 100% of the consequences with 0% of the control.

Bonafide inverts this model.

## How It Works

**Quantized encryption** — Personal data is decomposed into atomic units called Quanta. Each quantum has its own encryption key, access policy, and tamper-proof audit trail. Compromise of one reveals nothing about any other.

**Biometric-only identity** — The user's biometric, processed entirely on-device and never transmitted, is the sole key to the vault. No shared secrets exist anywhere in the system.

**Distributed vault hierarchy** — A user's vault is a tree of branches hosted across institutions. Each branch is cryptographically isolated. No institution sees the whole tree.

**20 graduated security levels** — From public identifiers (Level 0) to biometric roots (Level 20). Institutions access only the levels their relationship warrants. The ceiling is cryptographic, not policy.

**Blind validation** — Independent validators verify operations without seeing data, using zero-knowledge proofs. No single entity — including Sly Technologies — can access a user's vault.

**Unlinkable personas** — One biometric produces multiple cryptographically independent identities. No metadata, no correlation, no evidence the others exist.

**Content neutrality** — The vault encrypts, authorizes, and audits. It does not inspect content. No backdoors. No master keys. Lawful access is supported through audited, scoped overrides — not circumvention.

## Specification

The full specification is published across multiple parts:

| Part | Title | Scope |
|------|-------|-------|
| 1 | Foundation & Core Architecture | Vault hierarchy, quantum model, design principles |
| 2 | Cryptographic Foundation | Biometric hash hierarchy, key derivation, encryption layers |
| 3 | Security Levels & Authentication | 20-level model, elevation, quantum-level override |
| 4 | PII Protection & Privacy | Proxy identity, privacy scoring, canary detection |
| 5 | Blind Validation Network | Zero-knowledge validation, trust scoring, consensus |
| 6 | Infrastructure & Portfolio | Database packages, cloud coordination, ExaScale integration |
| 7 | Personas, Focus Profiles & Duress | Unlinkable personas, decoy vaults, cryptographic context isolation |
| 8 | Open Ecosystem & Governance | Namespace, federation, certification, governance evolution |
| 9 | Network Security & Abuse Prevention | Transport security, DoS defense, traffic analysis resistance |
| 10 | Enclave Architecture & Device Classes | Secure enclave tiers, device profiles, peripheral model, IoT |

## Ecosystem

Bonafide is a protocol, not a product. Anyone can build:

- **Vault providers** — compliant implementations for any market or jurisdiction
- **Validator nodes** — universities, NGOs, governments, privacy companies
- **Hardware** — FPGA enclaves, secure elements, dedicated consumer devices
- **Relay operators** — federated email/phone/address proxy services
- **Database plugins** — beyond the reference packages for PostgreSQL, Oracle, SQL Server, MySQL, MongoDB
- **Applications** — consumer apps, enterprise dashboards, wallets, browser extensions

### Certification

The [Bonafide Certified](https://bonafideid.org) program ensures interoperability:

- **Core Compliant** — basic spec conformance
- **Validator Certified** — blind validation operations
- **Relay Certified** — proxy relay services
- **Hardware Certified** — secure element and FPGA enclave
- **Privacy Verified** — institutional compliance audit

The specification is free. Reference implementations are open source. Certification requires verification — that's what funds ecosystem governance.

## Repositories

| Repository | Description |
|------------|-------------|
| `spec` | Canonical specification documents |
| `bonafide-core` | Reference implementation — vault protocol, key derivation, ledger, validation client |
| `bonafide-db` | Database-native vault packages (PostgreSQL, Oracle, SQL Server, MySQL, MongoDB) |
| `bonafide-sdk` | Client SDKs for application developers |
| `bonafide-relay` | Reference relay operator implementation |
| `bonafide-cert` | Certification test suites |

## Governance

**Phase 1 (current):** Sly Technologies stewards the specification and builds reference implementations.

**Phase 2:** When third-party implementers reach critical mass, the Bonafide Foundation assumes ownership of the spec, certification, and governance. Sly Technologies retains a permanent board seat but not a controlling vote.

**Phase 3:** The ecosystem operates independently of any single company.

## Domains

| Domain | Purpose |
|--------|---------|
| [bonafide.id](https://bonafide.id) | Network infrastructure, API, services |
| [bonafideid.org](https://bonafideid.org) | Specification, governance, certification, community |

## Status

> **Draft — February 2026**
>
> The specification is in active development. Bonafide is being implemented internally within Sly Technologies' ExaScale™ platform for initial validation with telco, banking, and defense customers before broader ecosystem release.

## License

The Bonafide specification is published as an open standard. Reference implementations are licensed under Apache 2.0.

## Contact

- **Specification & ecosystem:** [bonafideid.org](https://bonafideid.org)
- **Sly Technologies:** [slytechs.com](https://slytechs.com)
- **Security issues:** security@bonafide.id

---

*The last identity system you'll never have to remember.*
