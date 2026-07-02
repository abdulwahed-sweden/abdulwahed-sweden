<div align="center">

# Abdulwahed Mansour

**Rust Systems Engineer — I build production business systems in Rust**

Stockholm, Sweden · available for Rust projects — Swedish market & remote (EU)

[![Rust](https://img.shields.io/badge/Rust-000000?style=flat-square&logo=rust&logoColor=white)](#)
[![Tokio](https://img.shields.io/badge/Tokio-463f3a?style=flat-square&logo=rust&logoColor=white)](#)
[![Axum](https://img.shields.io/badge/Axum-8A2BE2?style=flat-square&logo=rust&logoColor=white)](#)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)](#)
[![WASM](https://img.shields.io/badge/WebAssembly-654FF0?style=flat-square&logo=webassembly&logoColor=white)](#)
[![PyO3](https://img.shields.io/badge/PyO3-FFD43B?style=flat-square&logo=rust&logoColor=black)](#)

</div>

---

I build **complete, deployable business systems in Rust** — not just libraries. Memory-safe services that a company can actually run: **one binary, one PostgreSQL, a full audit trail, no build step, and no frontend pipeline to maintain.**

My goal is simple: help **Swedish companies** replace fragile multi-service web stacks and per-seat SaaS with a single, auditable Rust system they own outright. 15+ years engineering, a zero-`unsafe` policy, and a security-research background mean the attack surface is part of the design from day one.

---

## 🦀 RustIO — my flagship

A **"Django-for-Rust"** framework I authored, and the products built on it.

**[rustio-admin](https://github.com/abdulwahed-sweden/rustio-admin)** — a Postgres-first administrative framework for Rust. Most admin tools treat CRUD as the product and bolt on auth later. RustIO inverts that: **authority — authentication, sessions, recovery, role-based access, and a complete audit trail — is designed as one system.** An admin surface is one derive, one impl, one register call.

- TOTP MFA + single-use Argon2id backup codes · re-auth wall on every destructive action
- Per-request `correlation_id` audit chain · 5-tier role hierarchy · account lockout + throttle
- **Postgres only. No build step. Single-binary deployment.**

**[rustio](https://github.com/abdulwahed-sweden/rustio)** — the web framework: plain Rust structs → a working admin UI, database, auth, and HTTP server, with a guided CLI that turns a one-sentence brief into a reviewed schema + migrations. Companion tooling: **[rustio-design](https://github.com/abdulwahed-sweden/rustio-design)** (declarative design system → `tokens.css`) and **[rustio-draft](https://github.com/abdulwahed-sweden/rustio-draft)** (natural-language brief → schema).

---

## 💼 What I build for Swedish companies

Built on rustio-admin, delivered as one memory-safe binary:

- **Business systems & internal control panels** — CRM, operations, back-office. One source of truth, audit-grade, no SaaS subscription and a radically smaller operational + attack surface.
- **Compliance-driven systems** — e.g. a self-hosted **EU Whistleblower Directive** channel (Swedish *lag 2021:890*, mandatory at 50+ staff) where data never leaves the company's own server; GDPR-aware data architecture.
- **Performance rescue** — embed a Rust core into an existing Python/Node service via **PyO3/FFI** to fix a hot path without a full rewrite.
- **Security & forensic tooling** — high-throughput analysis engines and bots as single, statically-linked binaries.

---

## 📦 Products & projects built on RustIO

**[SystemKraft](https://github.com/abdulwahed-sweden/systemkraft)** — business-systems engineering for Swedish enterprises. A public site *and* a live, fully-audited `/admin` CRM served from **one Rust binary** — the offering, running live.

**[Lursystem](https://github.com/abdulwahed-sweden/lursystem)** *(in development)* — self-hosted EU whistleblower-reporting & case-handling for Swedish employers; data stays in-country, behind the company's own audit chain.

**[clinicflow](https://github.com/abdulwahed-sweden/clinicflow)** · **[obddesk](https://github.com/abdulwahed-sweden/obddesk)** · **[shop](https://github.com/abdulwahed-sweden/shop)** — vertical demos proving the framework across clinic, diagnostics, and retail domains.

---

## 🔧 Other Rust work

**[polaris-chronos](https://github.com/abdulwahed-sweden/polaris-chronos)** — high-precision solar/prayer-time engine, polar-region capable; **Rust + WASM**, REST API, 96 tests, live on Hugging Face Spaces.

**[huntkey](https://github.com/abdulwahed-sweden/huntkey)** — intent-based sovereign smart account (ERC-4337); Rust + Solidity, 4-layer defense, 126 tests.

**[chthonic](https://github.com/abdulwahed-sweden/chthonic)** — modular, async-first penetration-testing framework in Rust.

**[swiftline](https://github.com/abdulwahed-sweden/swiftline)** · **[axum-rust](https://github.com/abdulwahed-sweden/axum-rust)** · **[deepseek-rust](https://github.com/abdulwahed-sweden/deepseek-rust)** · **[rust-scraper-pro](https://github.com/abdulwahed-sweden/rust-scraper-pro)** — CLI, web, async-client, and scraping libraries.

---

## 🛡️ Security research

Active on **Immunefi**, **Sherlock**, and **Code4rena** with confirmed findings in production systems — **$140K+ in bounties** and a discovered vulnerability *class* affecting **$98.6M+** across major DeFi protocols. Forensics: traced a **$1.5B** on-chain theft (42,479 addresses) in 36 seconds with a Rust engine.

---

## 🧰 Tech

**Rust:** Tokio · Axum · Serde · Rayon · Clap · Ratatui · PyO3 (Rust↔Python) · WASM · single-binary distribution · zero-`unsafe` · strict Clippy
**Data:** PostgreSQL (Postgres-first) · Redis · schema/migrations · audit trails
**Ops:** Docker · GitHub Actions CI/CD · Linux server hardening
**Also:** Solidity/Foundry (audits) · TypeScript

---

<div align="center">

**[abdulwahed.mansour@gmail.com](mailto:abdulwahed.mansour@gmail.com)** · **[LinkedIn](https://linkedin.com/in/abdulwahed-sweden)**

*Available for Rust engineering projects & consulting — Swedish market and remote across the EU.*

</div>
