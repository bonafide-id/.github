# Bonafide™

**Privacy by architecture, not by promise.**

Bonafide is an open specification for user-sovereign encrypted data vaults. Every piece of personal data is independently encrypted, secured by passwordless multi-factor authentication with hardware-bound biometrics, and distributed across institutions that can see only what the user authorizes. No passwords. No recovery phrases. No master keys. No central authority that can be compelled to decrypt.

Institutions don't protect your data behind their walls — they host encrypted fragments they cannot read.

---

## The Problem

Every major breach shares the same root cause: centralized databases full of plaintext personal data, protected by perimeter security that eventually fails. Users bear 100% of the consequences with 0% of the control.

Bonafide inverts this model.

## How It Works

**Quantized encryption** — Personal data is decomposed into atomic units called Quanta. Each quantum has its own encryption key, access policy, and tamper-proof audit trail. Compromise of one reveals nothing about any other.

**Passwordless multi-factor** — No passwords. No recovery phrases. No shared secrets. Bonafide uses hardware-bound biometric authentication that exceeds conventional MFA: the user's biometric (inherence) is processed entirely on-device within an attested secure element (possession), combined with a user-chosen root secret (knowledge) that is stored in the hardware enclave after initial setup. The root secret can be derived from composable authentication gestures — a spoken word, a specific fingerprint, a facial expression, a keystroke rhythm, a tap pattern, or any combination the user chooses. Daily authentication is a single touch; the device applies the stored root secret transparently. The entire derivation is stateless — there is no stored "correct answer," no error on failure, no oracle for an attacker to probe.

**Distributed vault hierarchy** — A user's vault is a tree of branches hosted across institutions. Each branch is cryptographically isolated. No institution sees the whole tree.

**Graduated security levels** — Extensible, cryptographic security levels from public identifiers up through sovereign biometric roots. Institutions access only the levels their relationship warrants. The ceiling is cryptographic, not policy — enforced by key derivation depth and enclave tier requirements. Deployments define as many or as few levels as their use case demands.

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

## Repositories

### Naming Convention

```
bonafide-{component}                → language-agnostic (spec, protocol, docs)
bonafide-{component}-{language}     → language-specific libraries
bonafide-{component}-{platform}     → platform-specific apps
bonafide-{service}                  → backend services
```

### Specification & Protocol

| Repository | Description |
|------------|-------------|
| [`bonafide-spec`](https://github.com/bonafide-id/bonafide-spec) | Canonical specification documents (all parts) |
| [`bonafide-protocol`](https://github.com/bonafide-id/bonafide-protocol) | Wire protocol definitions, protobuf/schema files, IDL |

### Core Libraries

The `core` libraries implement the Bonafide specification: key derivation, quantum encryption/decryption, Merkle operations, ledger format, and session management. Same protocol compliance, language-native idioms.

| Repository | Language | Notes |
|------------|----------|-------|
| [`bonafide-core-java`](https://github.com/bonafide-id/bonafide-core-java) | Java / Kotlin (JVM) | ExaScale integration, Android foundation |
| [`bonafide-core-c`](https://github.com/bonafide-id/bonafide-core-c) | C | FPGA host interface, embedded, IoT peripherals |
| [`bonafide-core-js`](https://github.com/bonafide-id/bonafide-core-js) | JavaScript / TypeScript | Node.js + browser, web vault foundation |
| [`bonafide-core-python`](https://github.com/bonafide-id/bonafide-core-python) | Python | Tooling, scripting, data science integrations |
| [`bonafide-core-swift`](https://github.com/bonafide-id/bonafide-core-swift) | Swift | iOS, macOS, Apple platform native |
| [`bonafide-core-kotlin`](https://github.com/bonafide-id/bonafide-core-kotlin) | Kotlin Multiplatform | Android-first, cross-platform mobile |
| [`bonafide-core-rust`](https://github.com/bonafide-id/bonafide-core-rust) | Rust | Systems, WASM, embedded, performance-critical |
| [`bonafide-core-go`](https://github.com/bonafide-id/bonafide-core-go) | Go | Services, infrastructure, validator nodes |

### Developer SDKs

SDKs wrap core libraries with ergonomic APIs, error handling, retry logic, and integration guides. Core is the engine — SDKs are the developer experience.

| Repository | Language |
|------------|----------|
| [`bonafide-sdk-js`](https://github.com/bonafide-id/bonafide-sdk-js) | JavaScript / TypeScript |
| [`bonafide-sdk-java`](https://github.com/bonafide-id/bonafide-sdk-java) | Java / Kotlin |
| [`bonafide-sdk-python`](https://github.com/bonafide-id/bonafide-sdk-python) | Python |
| [`bonafide-sdk-swift`](https://github.com/bonafide-id/bonafide-sdk-swift) | Swift |

### Database Packages

Vault schema, stored procedures, and extensions for each supported database.

| Repository | Database |
|------------|----------|
| [`bonafide-db-postgres`](https://github.com/bonafide-id/bonafide-db-postgres) | PostgreSQL |
| [`bonafide-db-oracle`](https://github.com/bonafide-id/bonafide-db-oracle) | Oracle |
| [`bonafide-db-sqlserver`](https://github.com/bonafide-id/bonafide-db-sqlserver) | SQL Server |
| [`bonafide-db-mysql`](https://github.com/bonafide-id/bonafide-db-mysql) | MySQL |
| [`bonafide-db-mongodb`](https://github.com/bonafide-id/bonafide-db-mongodb) | MongoDB |

### Services

Backend components for running Bonafide infrastructure.

| Repository | Description |
|------------|-------------|
| [`bonafide-gateway`](https://github.com/bonafide-id/bonafide-gateway) | API gateway — tiered authentication, rate limiting, request routing |
| [`bonafide-validator`](https://github.com/bonafide-id/bonafide-validator) | Reference validator node — blind validation, trust scoring, consensus |
| [`bonafide-relay`](https://github.com/bonafide-id/bonafide-relay) | Reference relay operator — email, phone, address proxy federation |
| [`bonafide-federation`](https://github.com/bonafide-id/bonafide-federation) | Federation coordination — cross-region sync, validator orchestration |
| [`bonafide-ledger`](https://github.com/bonafide-id/bonafide-ledger) | QuantaLedger service — immutable audit trail, Merkle root management |

### Applications

| Repository | Platform | Description |
|------------|----------|-------------|
| [`bonafide-app-ios`](https://github.com/bonafide-id/bonafide-app-ios) | iOS | Consumer vault app — Secure Enclave integration, Face ID / Touch ID |
| [`bonafide-app-android`](https://github.com/bonafide-id/bonafide-app-android) | Android | Consumer vault app — StrongBox / TrustZone, BiometricPrompt |
| [`bonafide-app-desktop`](https://github.com/bonafide-id/bonafide-app-desktop) | Windows / macOS / Linux | Desktop vault app — TPM, Secure Enclave, SGX support |
| [`bonafide-app-web`](https://github.com/bonafide-id/bonafide-app-web) | Browser | Web vault dashboard — WebAuthn, SubtleCrypto |
| [`bonafide-app-cli`](https://github.com/bonafide-id/bonafide-app-cli) | Terminal | Command-line vault management and developer tool |

### Tooling & Ecosystem

| Repository | Description |
|------------|-------------|
| [`bonafide-cert`](https://github.com/bonafide-id/bonafide-cert) | Certification test suites for all compliance tiers |
| [`bonafide-devtools`](https://github.com/bonafide-id/bonafide-devtools) | Developer tools — mock vault, local test network, sandbox environment |
| [`bonafide-docs`](https://github.com/bonafide-id/bonafide-docs) | Documentation site source (docs.bonafide.id) |
| [`bonafide-hardware`](https://github.com/bonafide-id/bonafide-hardware) | Hardware reference designs, FPGA bitstream specifications, enclave interfaces |

## Ecosystem

Bonafide is a protocol, not a product. Anyone can build:

- **Vault providers** — compliant implementations for any market or jurisdiction
- **Validator nodes** — universities, NGOs, governments, privacy companies
- **Hardware** — FPGA enclaves, secure elements, dedicated consumer devices
- **Relay operators** — federated email/phone/address proxy services
- **Database plugins** — beyond the reference packages listed above
- **Applications** — consumer apps, enterprise dashboards, wallets, browser extensions

### Certification

The [Bonafide Certified](https://bonafideid.org) program ensures interoperability:

- **Core Compliant** — basic spec conformance
- **Validator Certified** — blind validation operations
- **Relay Certified** — proxy relay services
- **Hardware Certified** — secure element and FPGA enclave
- **Privacy Verified** — institutional compliance audit

The specification is free. Reference implementations are open source. Certification requires verification — that's what funds ecosystem governance.

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
> The specification is in active development. Bonafide is being implemented internally within Sly Technologies' [ExaScale™](https://slytechs.com) platform for initial validation with telco, banking, and defense customers before broader ecosystem release.

## License

The Bonafide specification is published as an open standard. Reference implementations are licensed under Apache 2.0.

## Contact

- **Specification & ecosystem:** [bonafideid.org](https://bonafideid.org)
- **Sly Technologies:** [slytechs.com](https://slytechs.com)
- **Security issues:** security@bonafide.id

---

*The last identity system you'll never have to remember.*
