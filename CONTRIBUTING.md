# GLASTOR® Core Contributing Guidelines

Thank you for contributing to **GLASTOR® Core**. We value technical excellence, architectural rigor,
sub-millisecond efficiency, and clean engineering practices across our Rust, TypeScript/Deno, and
WebAssembly ecosystem.

---

## Key Governance Links

Before contributing, please familiarize yourself with:

- [Governance Model](GOVERNANCE.md) — Roles, merge authority, and RFC process.
- [Public Roadmap](ROADMAP.md) — Current priorities, milestones, and strategic direction.
- [Code of Conduct](CODE_OF_CONDUCT.md) — Community standards and expectations.
- [Security Policy](SECURITY.md) — Reporting vulnerabilities responsibly (never open a public issue).

---

## Finding Work, Reporting Bugs & RFCs

- **First-Time Contributors:** Browse issues labeled `good first issue` or `help wanted` across
  [`glastor-core` repositories](https://github.com/glastor-core). Comment on an issue before
  starting work to avoid duplicate effort.
- **Reporting Bugs:** Use the repository's issue template and include reproduction steps, OS and
  toolchain versions (`rustc --version`, `deno --version`, `node -v`), and minimal logs.
- **Major Features & Breaking Changes (RFCs):** Open a **GitHub Discussion** or **Issue** before
  implementing large architectural changes so maintainers can align on design and scope early.

---

## Fork, Branch & Pull Request Workflow

1. **Fork & Clone:**
   ```bash
   git clone https://github.com/<your-username>/<repo>.git
   cd <repo>
   git remote add upstream https://github.com/glastor-core/<repo>.git
   git fetch upstream && git rebase upstream/main
   ```

2. **Semantic Branching:**
   ```bash
   git checkout -b feat/your-feature-name
   # or fix/issue-description | perf/... | docs/... | refactor/...
   ```

3. **Local Hygiene & Verification:** Ensure formatting, linter, and tests pass with zero warnings
   before opening a PR:
   ```bash
   # Rust (Cargo workspaces: pii-veil, spec-stream, byte-gauge, specter, strata, hyper64)
   cargo fmt --all -- --check
   cargo clippy --workspace --all-targets -- -D warnings
   cargo test --workspace

   # Deno (glastor-core, nemesis, vortex, zerho, medusa, hyper-flow)
   deno fmt --check && deno lint && deno test -A

   # Bun / Node / pnpm
   pnpm run lint && pnpm test
   ```

4. **Conventional Commits & Sign-Off:** Follow our [Commit Convention](COMMIT_CONVENTION.md)
   (use `-s` for DCO sign-off and `-S` for GPG/SSH signing when configured):
   ```bash
   git commit -s -m "feat(core): implement deterministic schema validation"
   ```

5. **Open Pull Request:** Push to your fork and submit against `main` using our
   [PR Template](PULL_REQUEST_TEMPLATE.md), linking related issues (e.g. `Closes #12`).

---

## AI-Assisted Contributions Policy

AI-assisted tools are welcome as long as the contributor retains full ownership of the change:

- You have reviewed, understood, and can explain every line submitted.
- All local linters (`clippy` / `deno lint`), formatters, and tests pass cleanly.
- Unverified, hallucinated, or low-effort drive-by PRs will be closed.

---

## Automated CI Gates & Review Expectations

Pull Requests are automatically verified by:

- **CI Test Matrix:** Formatting, lints, and cross-platform test suites.
- **Nemesis (`glastor-core/nemesis`):** DevSecOps posture, secret scanning, and repo hygiene.
- **Specter (`glastor-core/specter`):** Zero-compiler AST API contract diff & Trojan Breaking Change guard.
- **Byte-Gauge (`glastor-core/byte-gauge`):** SIMD binary/Wasm hardening (`checksec`), entropy & SBOM.
- **CodeQL & OpenSSF Scorecard:** SAST and supply-chain verification.

---

## Engineering Principles & Licensing (DCO)

- **Clean Code & SOLID:** Modular, deterministic functions and strict typing without unjustified `any`.
- **Atomic Pull Requests:** One PR solves one discrete responsibility with unit/integration tests.
- **Documentation Parity:** Public API changes must include corresponding documentation updates.
- **Supply Chain Integrity:** Zero unjustified external dependencies. Keep footprint minimal.
- **License & DCO:** By submitting a contribution, you certify compliance with the
  [Developer Certificate of Origin](https://developercertificate.org/) and agree to license your
  contribution under the repository's license (**MIT** and/or **Apache-2.0**).

---

<sub>© 2026 GLASTOR® Core. All rights reserved. Licensed under Apache-2.0 / MIT.</sub>
