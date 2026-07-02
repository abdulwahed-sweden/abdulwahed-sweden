<div align="center">

# Abdulwahed Mansour

### Rust Systems Engineer · Offensive Security · On-Chain Forensics

**I build the software other engineers are afraid to write — in Rust, safe by construction.**

Stockholm, Sweden · 15+ years · zero&nbsp;`unsafe` · available for Rust projects (Swedish market & remote EU)

<br>

[![Lines of Rust & code](https://img.shields.io/badge/~208K-lines_shipped-000000?style=for-the-badge&logo=rust&logoColor=white)](#)
[![Tests](https://img.shields.io/badge/5%2C700%2B-automated_tests-2E7D32?style=for-the-badge)](#)
[![Traced](https://img.shields.io/badge/%241.5B-traced_in_36s-B71C1C?style=for-the-badge)](#)
[![Bounties](https://img.shields.io/badge/%24140K%2B-bounties_paid-6A1B9A?style=for-the-badge)](#)
[![Vuln class](https://img.shields.io/badge/%2498.6M-vuln_class_found-C62828?style=for-the-badge)](#)

[![Authorized security researcher](https://img.shields.io/badge/Authorized_Security_Researcher-Immunefi_·_Sherlock_·_Code4rena-1565C0?style=for-the-badge&logo=hackerone&logoColor=white)](#)
[![Immunefi Hall of Fame](https://img.shields.io/badge/🏆_Immunefi-Hall_of_Fame-FF6B00?style=for-the-badge)](#)

</div>

---

I don't write toy programs. I ship **production systems in Rust** where correctness is not optional: red-team platforms, blockchain forensic engines that compete with Chainalysis, DeFi protocols guarded by formal invariants, and a full web + admin framework. Every line under a **zero-`unsafe` policy** and the strictest Clippy configuration — power *and* safety, at the same time.

For companies, that translates into one thing: **memory-safe business systems you can actually run** — one binary, one PostgreSQL, a complete audit trail, no build step, no per-seat SaaS bill. My goal is to bring that to the **Swedish market** through the RustIO project below.

---

## 🦀 RustIO — the framework I authored

> **"Django-for-Rust."** Plain Rust structs in → a working admin UI, database, auth, and HTTP server out. Then I ship real business systems on it.

**[`rustio-admin`](https://github.com/abdulwahed-sweden/rustio-admin)** · **[`rustio`](https://github.com/abdulwahed-sweden/rustio)** · **[`rustio-draft`](https://github.com/abdulwahed-sweden/rustio-draft)** · **[`rustio-design`](https://github.com/abdulwahed-sweden/rustio-design)**

Most admin tools treat CRUD as the product and bolt on auth later. **RustIO inverts that** — *authority* (authentication, sessions, recovery, role-based access, complete audit trail) is designed as **one system**:

`TOTP MFA + Argon2id backup codes` · `re-auth wall on every destructive action` · `per-request correlation_id audit chain` · `5-tier RBAC` · `account lockout + throttle` · **`single-binary · no build step · no frontend pipeline`**

Live products on it → **[SystemKraft](https://github.com/abdulwahed-sweden/systemkraft)** (business systems for Swedish enterprises) · **[Lursystem](https://github.com/abdulwahed-sweden/lursystem)** (EU whistleblower compliance, *lag 2021:890*) · **[clinicflow](https://github.com/abdulwahed-sweden/clinicflow)** · **[obddesk](https://github.com/abdulwahed-sweden/obddesk)** · **[shop](https://github.com/abdulwahed-sweden/shop)**

---

## ⚔️ The Arsenal — my most powerful Rust systems

| System | What it is | The numbers that matter |
|--------|-----------|--------------------------|
| **[Ferox](https://github.com/abdulwahed-sweden/ferox)** `v4.1` | Rust-native offensive-security / red-team platform | **94K+ LOC** · **782+ tests** · **36-crate** enterprise edition · **33+** post-exploitation modules · zero `unsafe` |
| 🔒 **Ferox-Pro** `v2.2` | Enterprise security-assessment engine | Nuclei-compatible template engine · CVSS 3.1 / CWE / CVE · REST API for CI/CD · EVM **&** Solana contract analysis |
| **[BTC Sentinel](https://github.com/abdulwahed-sweden/Bitcoin-Sentinel)** `v2.0` | Multi-chain forensic intelligence — *"Chainalysis at zero cost"* | **20,000 tx/s** analysis · **50,000 addr/s** clustering · **<1 ms** wire-speed mempool intercept |
| 🔒 **Amend Protocol** | Multi-chain DeFi vault suite (EVM + Solana) | **1,630 tests** incl. **1,000-run fuzz** · on-chain ethics invariants (`EthicsGuard`, `FairFeeGuard`) |
| **[HuntKey](https://github.com/abdulwahed-sweden/huntkey)** | Sovereign smart account (ERC-4337) | **126 tests** · **15 on-chain checks** · 4-layer defense · no blind signing, no long-lived keys |

<div align="center"><sub>🔒 = private / enterprise repository — walkthrough available on request</sub></div>

### 🎯 Career-defining result

> **Traced the $1.5B Bybit / Lazarus theft — 42,479 addresses across 33 clusters — in 36 seconds**, with a single statically-linked Rust binary (zero-copy parsing, zero-allocation hot paths). Aave V3 liquidation research spanned **33,827 on-chain events**.

---

## 🕸️ Web3 · Smart-Contract Security

> ### ✅ Authorized Security Researcher · 🏆 Immunefi Hall of Fame
> **Listed in the Immunefi Hall of Fame.** I operate **exclusively under sanctioned bug-bounty & audit programs** — with explicit authorization from the industry's leading platforms, **Immunefi · Sherlock · Code4rena** — and have **confirmed, paid findings in the production systems of major protocols**, including **Aave**, **Morpho**, **Curve**, and **ENS**. Every engagement is legal, in-scope, and permissioned.

Offensive research that pays: **$140K+ in confirmed bounties** on Immunefi, Sherlock & Code4rena — and a discovered **vulnerability *class* affecting $98.6M+** (Anti-Dilution / ADS) across **Aave V4**, **Morpho Blue**, and **Curve crvUSD**.

| Platform | Target | Finding | Severity |
|----------|--------|---------|----------|
| Research | Aave V4 | ADS phantom-yield extraction (~$96M) | **Critical** |
| Research | Morpho Blue | ADS invariant violations (~$2M) | **Critical** |
| Research | Curve crvUSD | ADS fee asymmetry (~$585K) | **Critical** |
| Immunefi | Moonwell / Mamo | SlippagePriceChecker boundary condition | High |
| Immunefi | ENS | Gas griefing in `SignatureUtils.sol` | Medium |

Also shipping: 🔒 **HuntLoan** — MEV flash-loan liquidation bot **deployed live on Base mainnet** (HF-velocity prediction, 3-tier × 3-regime gas strategy, circuit breaker) · 🔒 **fluid-tick-drift-guard** — oracle-manipulation defense **proven against a $50M mainnet-fork attack**.

---

## 🔧 Also in Rust

**[polaris-chronos](https://github.com/abdulwahed-sweden/polaris-chronos)** — solar/prayer-time engine, polar-region capable · **Rust + WASM** · 96 tests · live on HF Spaces
**[chthonic](https://github.com/abdulwahed-sweden/chthonic)** — modular async-first pentest framework · **[rust-scraper-pro](https://github.com/abdulwahed-sweden/rust-scraper-pro)** · **[swiftline](https://github.com/abdulwahed-sweden/swiftline)** · **[axum-rust](https://github.com/abdulwahed-sweden/axum-rust)** · **[deepseek-rust](https://github.com/abdulwahed-sweden/deepseek-rust)**

---

## 🧰 Stack

**Rust** Tokio · Axum · Serde · Rayon · Clap · Ratatui · **PyO3** (Rust↔Python) · **WASM** · Tauri · single-binary · zero&nbsp;`unsafe` · strict Clippy
**Chain** Solidity 0.8.x · Foundry · Anchor/Solana · `alloy` · ERC-4626 / ERC-4337 · MEV
**Data / Ops** PostgreSQL (Postgres-first) · Redis · Docker · GitHub Actions CI/CD · Linux hardening

---

<div align="center">

### Available for Rust engineering projects & consulting — Swedish market and remote across the EU.

**[abdulwahed.mansour@gmail.com](mailto:abdulwahed.mansour@gmail.com)** · **[LinkedIn](https://linkedin.com/in/abdulwahed-sweden)**

<sub>Power and safety are not a trade-off. I ship both.</sub>

</div>
