<div align="center">

# Abdulwahed Mansour

### Rust systems & framework engineer · Offensive-security & on-chain forensics

Stockholm, Sweden · available for Rust engineering — Swedish market & remote (EU)

[![Rust](https://img.shields.io/badge/Rust-000000?style=for-the-badge&logo=rust&logoColor=white)](#)
[![Multi-crate workspaces](https://img.shields.io/badge/4-multi--crate_workspaces-DEA584?style=for-the-badge)](#)
[![zero unsafe](https://img.shields.io/badge/zero-unsafe-2E7D32?style=for-the-badge)](#)
[![Authorized researcher](https://img.shields.io/badge/Authorized-Security_Researcher-1565C0?style=for-the-badge&logo=hackerone&logoColor=white)](#)
[![Immunefi Hall of Fame](https://img.shields.io/badge/🏆_Immunefi-Hall_of_Fame-FF6B00?style=for-the-badge)](#)

</div>

---

I build systems in Rust that are meant to **run**, not to demo — a web + admin framework, a **37-crate** security platform, a wire-speed blockchain forensic engine, a **14-crate** robotics control stack. Multi-crate workspaces, **`zero unsafe`**, strict Clippy, single-binary deployment.

I'm not asking to be considered a Rust engineer. The workspaces are here, the crate boundaries are here, the tests are here. **Read the code and judge the systems.**

---

## RustIO — a Rust web + admin framework (authored)

**The thesis:** most admin tools treat CRUD as the product and bolt on auth, sessions, recovery, and audit afterward. RustIO inverts that — **authority is designed as one system**: authentication, sessions, password recovery, role-based access, MFA, and a complete audit trail as a single, coherent layer. CRUD is the easy part on top. An admin surface is one derive, one impl, one register call.

`TOTP MFA + Argon2id backup codes` · `re-auth wall on every destructive action` · `per-request correlation_id audit chain` · `5-tier RBAC` · **`Postgres-first · single binary · no build step · no frontend pipeline`**

| Repo | | Verified structure |
|------|--|--------------------|
| **[rustio-admin](https://github.com/abdulwahed-sweden/rustio-admin)** | Postgres-first admin framework | **12-crate workspace**, 86% Rust, 152 Rust source files |
| **[rustio](https://github.com/abdulwahed-sweden/rustio)** | Web framework (structs → admin, DB, auth, HTTP) | **6-crate workspace**, 90% Rust |
| **[rustio-draft](https://github.com/abdulwahed-sweden/rustio-draft)** | Natural-language brief → schema | guided project genesis |

Demonstration surfaces built on it → **[systemkraft](https://github.com/abdulwahed-sweden/systemkraft)** · **[lursystem](https://github.com/abdulwahed-sweden/lursystem)** (EU whistleblower compliance, *lag 2021:890*) · **[clinicflow](https://github.com/abdulwahed-sweden/clinicflow)**

RustIO is open infrastructure. If you build on it, you can back its development → **[Sponsor RustIO](https://github.com/sponsors/abdulwahed-sweden)**.

> Framework authorship is proven by the *shape* of the code — a 12-crate workspace with derive macros and a registration API. The crates are **authored / beta**, not yet published to crates.io.

---

## Arsenal — the strongest systems

Ranked by technical force. Structural facts (crates, files, language mix) are **verified in-repo**; test counts are **declared in each project's README**.

| System | What it is | Evidence |
|--------|-----------|----------|
| 🔒 **Ferox-Pro** | Rust security-assessment platform (web crawler, Nuclei-compatible engine, REST API, EVM+Solana analysis) | **37-crate workspace** · 88% Rust · 351 Rust files · 622 files *(verified)* |
| **[Ferox](https://github.com/abdulwahed-sweden/ferox)** `v4.1` | Rust-native offensive-security framework (recon, exploitation, C2, memory forensics, Tauri desktop) | 74% Rust + Tauri UI · **206 Rust files** · MIT *(public — inspect it)* |
| **[Bitcoin-Sentinel](https://github.com/abdulwahed-sweden/Bitcoin-Sentinel)** `v2.0` | Multi-chain forensic engine — clustering, taint, mempool interception | Rust core · zero-copy / zero-alloc · **20,000 tx/s · 50,000 addr/s · <1 ms mempool** *(declared)* |
| **[robotics-platform](https://github.com/abdulwahed-sweden/robotics-platform)** | 5-DOF arm control: analytic IK, motion planning, state machine, URDF, sim↔hardware trait surface | **14-crate workspace** · 85% Rust *(public)* |
| **[chthonic](https://github.com/abdulwahed-sweden/chthonic)** | Async-first modular penetration-testing framework | **100% Rust** *(public)* |
| **[huntkey](https://github.com/abdulwahed-sweden/huntkey)** | Sovereign smart account (ERC-4337): no blind signing, no long-lived keys | Rust + Solidity · 15 on-chain checks · 126 tests *(declared)* |
| **[polaris-chronos](https://github.com/abdulwahed-sweden/polaris-chronos)** | Solar/prayer-time engine, polar-region capable | **Rust + WASM** · live on HF Spaces · 96 tests *(declared)* |

<div align="center"><sub>🔒 = private / enterprise repository — technical walkthrough available on request</sub></div>

Supporting Rust (public, single-purpose, clean): **[swiftline](https://github.com/abdulwahed-sweden/swiftline)** · **[rust-cli-toolkit](https://github.com/abdulwahed-sweden/rust-cli-toolkit)** · **[axum-rust](https://github.com/abdulwahed-sweden/axum-rust)** · **[deepseek-rust](https://github.com/abdulwahed-sweden/deepseek-rust)** · **[rust-scraper-pro](https://github.com/abdulwahed-sweden/rust-scraper-pro)**

---

## Security & Forensics

I operate **exclusively under sanctioned bug-bounty & audit programs** — with explicit authorization from the industry's leading platforms, **Immunefi · Sherlock · Code4rena** — and I am **listed in the Immunefi Hall of Fame**. Every engagement is legal, in-scope, and permissioned; findings are **responsibly disclosed** with reproducible PoCs. Offensive tools (Ferox, chthonic) are MIT-licensed for **authorized use only**.

Research highlight — a discovered **vulnerability *class*** (Anti-Dilution / ADS), responsibly disclosed:

| Target | Finding | Severity |
|--------|---------|----------|
| Aave V4 | ADS phantom-yield extraction | **Critical** |
| Morpho Blue | ADS invariant violations (3 types) | **Critical** |
| Curve crvUSD | ADS fee asymmetry | **Critical** |

Forensic result: traced the **Bybit / Lazarus theft — 42,479 addresses across 33 clusters, 682 transactions — in 36 seconds**, from a single statically-linked Rust binary. *(On-chain forensic conclusions are investigative leads, not legal proof.)*

---

## Numbers

**Verified in-repo (inspect the trees yourself):**
- **4 multi-crate Rust workspaces** — Ferox-Pro (37), robotics-platform (14), rustio-admin (12), rustio (6)
- Ferox: **206 Rust source files**, 74% Rust + Tauri UI
- rustio-admin: **86% Rust**, 152 Rust files · chthonic / swiftline / rust-cli-toolkit / axum-rust / deepseek-rust: **100% Rust**

**Declared in project READMEs (run the tests to confirm):**
- Bitcoin-Sentinel: 20,000 tx/s analysis · 50,000 addr/s clustering · <1 ms mempool
- Test suites: Ferox-Pro 782+ · huntkey 126 · Bitcoin-Sentinel 111 · polaris-chronos 96

---

## Stack

**Rust** Tokio · Axum · Serde · Rayon · Clap · Ratatui · **PyO3** (Rust↔Python) · **WASM** · Tauri · derive macros · single-binary · `zero unsafe` · strict Clippy
**Chain** Solidity 0.8.x · Foundry · Anchor/Solana · `alloy` · ERC-4626 / ERC-4337
**Data / Ops** PostgreSQL (Postgres-first) · Redis · Docker · GitHub Actions CI/CD · Linux hardening

---

<div align="center">

### Available for Rust engineering — Swedish market and remote across the EU.

**[abdulwahed.mansour@gmail.com](mailto:abdulwahed.mansour@gmail.com)** · **[LinkedIn](https://linkedin.com/in/abdulwahed-sweden)**

<sub>This is the work. Judge the code.</sub>

</div>
