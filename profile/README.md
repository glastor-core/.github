<div align="center">

# ⚡ GLASTOR® Core

**Sub-millisecond Rust security, AI privacy (`pii-veil`), and zero-compiler AST governance
(`specter`) — engineered by [glastor.es](https://glastor.es).**

[![CI](https://img.shields.io/github/actions/workflow/status/glastor-core/glastor-core/ci.yml?branch=main&style=for-the-badge&label=CI)](https://github.com/glastor-core/glastor-core/actions/workflows/ci.yml)
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg?style=for-the-badge)](https://github.com/glastor-core/glastor-core/blob/main/LICENSE)
[![OpenSSF Scorecard](https://img.shields.io/badge/OpenSSF%20Scorecard-Enforced-blue?style=for-the-badge)](https://github.com/glastor-core/glastor-core/actions/workflows/scorecard.yml)
[![pii-veil Live Demo](https://img.shields.io/badge/pii--veil-Live%20WASM%20Demo-00c896?style=for-the-badge)](https://pii-veil.glastor.es)
[![Specter AST](https://img.shields.io/badge/Specter-AST%20SemVer-8b5cf6?style=for-the-badge)](https://specter.glastor.es)
[![llms.txt](https://img.shields.io/badge/llms.txt-standard-8A2BE2?style=for-the-badge)](https://github.com/glastor-core/glastor-core/blob/main/llms.txt)
[![Official Domain](https://img.shields.io/badge/Web-glastor.es-0ea5e9.svg?style=for-the-badge)](https://glastor.es)
<br>
[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/glastor-core/glastor-core)
[![Watch on GitHub](https://img.shields.io/github/watchers/glastor-core/glastor-core?style=social&label=Watch)](https://github.com/glastor-core/glastor-core/watchers)
[![Fork on GitHub](https://img.shields.io/github/forks/glastor-core/glastor-core?style=social&label=Fork)](https://github.com/glastor-core/glastor-core/fork)
[![Star on GitHub](https://img.shields.io/github/stars/glastor-core/glastor-core?style=social)](https://github.com/glastor-core/glastor-core)
[![Follow @glastor-dev](https://img.shields.io/github/followers/glastor-dev?label=Follow%20%40glastor-dev&style=social)](https://github.com/glastor-dev)
[![Follow @glastor-core](https://img.shields.io/github/followers/glastor-core?label=Follow%20%40glastor-core&style=social)](https://github.com/glastor-core)

<p align="center">
  <a href="#features">Features</a> •
  <a href="#ecosystem">Flagship Projects</a> •
  <a href="https://github.com/glastor-core/glastor-core/blob/main/ECOSYSTEM.md">Ecosystem</a> •
  <a href="#architecture">Architecture</a> •
  <a href="#quick-start">Quick Start</a> •
  <a href="#security">Security</a> •
  <a href="#contributing">Contributing</a> •
  <a href="#discussions">Discussions</a> •
  <a href="#license">License</a>
</p>

---

</div>

<a id="features"></a>

## 🌟 Key Features & Highlights

- **⚡ Sub-Millisecond Rust Performance**: `165 µs` reversible PII/secret redaction (`pii-veil`) and
  `< 5 ms` zero-compiler polyglot AST diffing (`specter`) with `< 15 MB` memory footprint.
- **🔐 Reversible AI Privacy & Streaming (`pii-veil`)**: 18 mathematical checksum detectors (Luhn,
  IBAN Mod-97, SSN, DNI/CUIT), encrypted vaults, real-time SSE token restoration (`69.6 µs/chunk`),
  and built-in MCP server (`veil mcp`).
- **🔒 Zero-Trust API & Supply-Chain Guard (`specter`)**: Cryptographic public API fingerprinting
  (`SHA-256`), Trojan Breaking-Change detection, and mathematical SemVer enforcement across Rust &
  TypeScript.
- **📦 Polyglot & Multi-Channel Distribution**: Native crates (`crates.io`), Python (`PyPI`),
  Node.js (`npm`), Go SDK, WebAssembly ([`pii-veil.glastor.es`](https://pii-veil.glastor.es)),
  Homebrew, and Official MCP Registry.
- **🤖 DevSecOps & GitHub Actions Native**: Published on GitHub Marketplace with SARIF 2.1.0 Code
  Scanning, CycloneDX 1.5 SBOM, OpenSSF Scorecard, and automated CI governance.

---

<a id="ecosystem"></a>

## 🚀 Flagship Projects

| Project                                                    | Purpose                                                                                             | Key Benchmark / SLA                                                          | Links & Distribution                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| :--------------------------------------------------------- | :-------------------------------------------------------------------------------------------------- | :--------------------------------------------------------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **[`pii-veil`](https://github.com/glastor-core/pii-veil)** | Sub-millisecond reversible PII & secret anonymizer for LLMs, AI agents, MCP & real-time SSE streams | `165 µs` prompt latency (`212x` vs Presidio) · `69.6 µs` SSE · `< 15 MB` RAM | [![Live WASM Demo](https://img.shields.io/badge/Live%20Demo-pii--veil.glastor.es-00c896?style=flat-square)](https://pii-veil.glastor.es) [![crates.io](https://img.shields.io/crates/v/pii-veil-core?style=flat-square&color=orange)](https://crates.io/crates/pii-veil-core) [![GitHub](https://img.shields.io/github/stars/glastor-core/pii-veil?style=social)](https://github.com/glastor-core/pii-veil)                                                                                   |
| **[`specter`](https://github.com/glastor-core/specter)**   | Zero-compiler polyglot AST API contract differ, Trojan Breaking-Change detector & SemVer gatekeeper | `< 5 ms` Rust + TypeScript AST diff · SARIF 2.1.0 & CycloneDX 1.5 SBOM       | [![Marketplace](https://img.shields.io/badge/GitHub-Marketplace-blue?style=flat-square&logo=github-actions&logoColor=white)](https://github.com/marketplace/actions/glastor-specter-polyglot-ast-api-contract-semver-gatekeeper) [![crates.io](https://img.shields.io/crates/v/specter-cli?style=flat-square&color=orange)](https://crates.io/crates/specter-cli) [![GitHub](https://img.shields.io/github/stars/glastor-core/specter?style=social)](https://github.com/glastor-core/specter) |

> Looking for the full suite (`byte-gauge`, `spec-stream`, `strata`, `hyper64`, `vortex`, `nemesis`,
> `zerho`, `medusa`, `benchmarks`) and official README badges? See
> **[ECOSYSTEM.md](https://github.com/glastor-core/glastor-core/blob/main/ECOSYSTEM.md)** or visit
> **[github.com/glastor-core](https://github.com/glastor-core)**.

---

<a id="architecture"></a>

## 🏛️ Architecture Overview

<p align="center">
  <img src="https://res.cloudinary.com/dzualplqi/image/upload/v1795366061/Diagrama_de_Seguridad_GLASTOR_CORE_n5locs.png" alt="GLASTOR® Core Architecture" width="100%" />
</p>

---

<a id="quick-start"></a>

## 🚀 Quick Start (Try Our Flagships)

### 1. `pii-veil` — Sub-Millisecond Reversible PII & Secret Privacy

Try it zero-install in the browser at **[pii-veil.glastor.es](https://pii-veil.glastor.es)**, or install the native Rust CLI (`< 15 MB` RAM):

```bash
# Install the native Rust CLI
cargo install pii-veil-cli

# Start the local HTTP/SSE DLP reverse proxy or stdio MCP server (Claude / Cursor / Windsurf)
veil proxy --listen 127.0.0.1:8080 --echo
veil mcp
```

### 2. `specter` — Zero-Compiler AST API Contract & SemVer Gatekeeper

Drop directly into `.github/workflows/ci.yml` (`< 5 ms` Rust + TypeScript AST diff, SARIF 2.1.0 & CycloneDX 1.5 SBOM):

```yaml
- uses: glastor-core/specter@v1
  with:
    head-dir: "."
    fail-on-trojan: "true"
```

```bash
# Or install the CLI locally via crates.io
cargo install specter-cli
```

---

<a id="security"></a>

## 🔒 Security & Governance

We maintain strict zero-trust standards:

- **Push Protection**: Automated secret scanning blocks leaked credentials before commits reach
  `main`.
- **Branch Rules**: Direct pushes to `main` are disabled; all merges require peer review and green
  CI checks.
- **Vulnerability Reporting**: See [SECURITY.md](https://github.com/glastor-core/glastor-core/blob/main/SECURITY.md) for confidential advisory reporting
  procedures.
- **Engineering Leadership**: Directed by [@glastor-dev](https://github.com/glastor-dev) (**GitHub
  Developer Program Member**) under the official [glastor.es](https://glastor.es) engineering
  division.
- **Organization Governance**: Consult [GOVERNANCE.md](https://github.com/glastor-core/.github/blob/main/GOVERNANCE.md) for leadership
  structure, team roles, and RFC adoption rules.
- **Community Standards**: Enforced across all community interactions via
  [CODE_OF_CONDUCT.md](https://github.com/glastor-core/glastor-core/blob/main/CODE_OF_CONDUCT.md).

---

<a id="discussions"></a>

## 💬 Discussions & Support

Need assistance or have an architectural idea?

- Join the community in [GitHub Discussions](https://github.com/orgs/glastor-core/discussions).
- Review our [Support Guidelines](https://github.com/glastor-core/glastor-core/blob/main/SUPPORT.md) for community channels and SLA details.
- For enterprise & commercial inquiries: [`founder@glastor.es`](mailto:founder@glastor.es) •
  [glastor.es](https://glastor.es).

---

<a id="contributing"></a>

## 🤝 Contributing

We welcome contributions! Please consult the [Contributing Guide](https://github.com/glastor-core/glastor-core/blob/main/CONTRIBUTING.md) to learn about
our branch standards, commit formatting (`feat:`, `fix:`, etc.), and test coverage expectations.
Check our [Public Roadmap](https://github.com/glastor-core/.github/blob/main/ROADMAP.md) for active milestones.

> 🔔 **Stay Updated on Releases**: Click **Watch** (top-right) and select **Custom ➔ Releases** for
> core runtime releases and architectural RFCs.

---

<a id="citation"></a>

## 📜 Citation

If you use **GLASTOR® Core** in your research or production systems, please cite it using
[`CITATION.cff`](https://github.com/glastor-core/glastor-core/blob/main/CITATION.cff).

---

<a id="license"></a>

## 📄 License

Distributed under the **Apache License 2.0**. See [`LICENSE`](https://github.com/glastor-core/glastor-core/blob/main/LICENSE) for full details.

<div align="center">
  <sub>© 2010–2026 <a href="https://glastor.es">GLASTOR®</a> (INPI Reg. 4559568 & 4559567) • Dual-Hub Operations (Spain & Argentina · Export Invoice Factura E) • Led by <a href="https://github.com/glastor-dev">@glastor-dev</a> (GitHub Developer Program Member).</sub>
</div>
