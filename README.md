<div align="center">

# Abdulwahed Mansour

**Smart Contract Security Researcher · Rust Systems Engineer · Protocol Architect**

[![Rust](https://img.shields.io/badge/Rust-2024%20Edition-F74C00?style=flat-square&logo=rust&logoColor=white)](#)
[![Solidity](https://img.shields.io/badge/Solidity-0.8+-363636?style=flat-square&logo=solidity&logoColor=white)](#)
[![ERC-4337](https://img.shields.io/badge/ERC--4337-Account%20Abstraction-3C3C3D?style=flat-square&logo=ethereum&logoColor=white)](#)
[![Tests](https://img.shields.io/badge/Tests-5,700+-brightgreen?style=flat-square)](#)
[![Security](https://img.shields.io/badge/Security-Defense%20in%20Depth-critical?style=flat-square)](#)
[![License](https://img.shields.io/badge/License-MIT-blue?style=flat-square)](#)

[![Email](https://img.shields.io/badge/Email-abdulwahed.sweden%40gmail.com-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:abdulwahed.sweden@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-abdulwahed--mansour-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/in/abdulwahed-mansour)
[![Immunefi](https://img.shields.io/badge/Immunefi-Bug%20Bounty-3b82f6?style=flat-square)](#)
[![Sherlock](https://img.shields.io/badge/Sherlock-Auditor-8B5CF6?style=flat-square)](#)

</div>

---

Independent security researcher specializing in DeFi protocol vulnerabilities, ERC-4337 account abstraction, and smart contract auditing. I combine rigorous economic modeling with systems-level Rust engineering — building property-based fuzzers, formal invariant proofs, and exploit simulators to find what static analyzers miss.

38 projects · 208,000 lines of code · 5,700+ tests across Rust, Solidity, Python, and TypeScript.

Currently focused on: **intent-based account abstraction**, **blockchain forensics**, **ZK credential systems**, **Asymmetric Deficit Socialization (ADS)** in lending protocols, and **Shariah-compliant DeFi infrastructure**.

---

## What I Build

| Blockchain Security | Forensics & Intelligence | Protocol Architecture |
|:-------------------:|:------------------------:|:---------------------:|
| Smart contract auditing | On-chain crime tracing | DeFi vaults & lending |
| Oracle manipulation defense | MITRE ATT&CK mapping | ERC-4337 account abstraction |
| MEV research & mitigation | AML tooling & mempool analysis | Islamic finance primitives |

---

## Flagship Projects

<table>
<tr>
<td width="50%" valign="top">

### [`huntkey`](https://github.com/abdulwahed-sweden/huntkey)
**Intent-Based Sovereign Smart Account Protocol**

ERC-4337 Account Abstraction with a 4-layer defense-in-depth execution model. Session keys are HKDF-derived, single-use, and chain-isolated — the master key never touches the network. 15 on-chain validation checks per transaction.

`Rust` `Solidity` `ERC-4337` `EIP-712` `ZK Claims` `126 tests`

</td>
<td width="50%" valign="top">

### [`Bitcoin-Sentinel`](https://github.com/abdulwahed-sweden/Bitcoin-Sentinel)
**Blockchain Forensics Platform**

Multi-chain forensics for tracing criminal fund flows across Bitcoin and Ethereum. Live mempool interception, MITRE ATT&CK tactic mapping, and a built-in threat intelligence database. Traced the $1.5B Bybit hack in 36 seconds.

`Rust` `Python` `MITRE ATT&CK` `AML` `213 tests`

</td>
</tr>
<tr>
<td width="50%" valign="top">

### [`fluid-tick-drift-guard`](https://github.com/abdulwahed-sweden/fluid-tick-drift-guard)
**Oracle Manipulation Defense**

Solidity library blocking Uniswap V3 tick drift oracle attacks. Dual-layer defense using EIP-1153 transient storage (per-tx) and permanent storage (per-block). Proven on a $50M mainnet fork simulation.

`Solidity` `EIP-1153` `Foundry` `Cancun EVM` `20 tests`

</td>
<td width="50%" valign="top">

### [`amend`](https://github.com/abdulwahed-sweden/amend)
**Multi-Chain DeFi Vault Protocol**

Cross-chain vault protocol across EVM and Solana with 1,630 tests. Introduces EthicsGuard and FairFeeGuard — on-chain invariants encoding ethical constraints that governance cannot override.

`Solidity` `Rust` `Anchor` `ERC-4626` `1,630 tests`

</td>
</tr>
<tr>
<td width="50%" valign="top">

### [`sunna-protocol`](https://github.com/abdulwahed-sweden/sunna-protocol)
**Shariah-Compliant DeFi Infrastructure**

Built around the ADS vulnerability class I discovered (~$98.6M exposure). First protocol with on-chain JHD effort measurement, Mudaraba profit-loss sharing, and constitutional governance boundaries no token vote can override.

`Solidity` `Foundry` `Islamic Finance` `124 tests`

</td>
<td width="50%" valign="top">

### [`polaris-chronos`](https://github.com/abdulwahed-sweden/polaris-chronos)
**Universal Prayer Time Engine**

Islamic astronomical engine solving prayer calculation in polar regions where standard algorithms break. Odeh (2004) crescent visibility criterion, adaptive projection for Midnight Sun and Polar Night. Deployed on Hugging Face.

`Rust` `Astronomy` `Hugging Face` `109 tests`

</td>
</tr>
</table>

---

## Security Research & Findings

### Vulnerability Discovery

**ADS (Asymmetric Deficit Socialization)** — Vulnerability class I discovered and formalized. Affects fee extraction during unrealized loss periods. ~$98.6M phantom yield exposure across Aave V4, Morpho Blue, and Curve crvUSD.

### Audit Results

| Contest / Program | Finding | Severity |
|-------------------|---------|----------|
| **Fluid DEX V2** (Sherlock) | Liquidation dust debt creates uncloseable positions | Low–Medium |
| **Fluid DEX V2** (Sherlock) | Smart Debt round-trip precision loss (1–2 wei leak) | Informational |
| **Fluid DEX V2** (Sherlock) | BigMath accounting mismatch (team-acknowledged DC#13) | Informational |
| **Moonwell / Mamo** | SlippagePriceChecker vulnerability | High |

### Blockchain Forensics

| Investigation | Scale | Outcome |
|---------------|-------|---------|
| **Bybit Hack** (DELTA STRIKE) | $1.5B · 682 txs · 42,479 addresses | Lazarus Group attribution, THORChain/Chainflip bridge tracing |
| **DSI Hack** | Decentralized Systems Inc | Full fund flow reconstruction |

---

## GitHub Stats

<div align="center">

[![GitHub Stats](https://github-readme-stats.vercel.app/api?username=abdulwahed-sweden&show_icons=true&theme=github_dark&hide_border=true&count_private=true&include_all_commits=true&rank_icon=github)](https://github.com/abdulwahed-sweden)
&nbsp;
[![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=abdulwahed-sweden&layout=compact&theme=github_dark&hide_border=true&langs_count=8)](https://github.com/abdulwahed-sweden)

</div>

---

## Stack

```
Security Research    Foundry · Slither · Echidna · Hypothesis · Custom Fuzzers
Smart Contracts      Solidity · EVM Internals · OpenZeppelin 5.0 · ERC-4337
Protocol Design      EIP-712 · Account Abstraction · ZK Claims · HKDF-SHA256
Systems Engineering  Rust · Tokio · Axum · async-std
Blockchain           EVM · Solana · Bitcoin · DeFi Protocol Architecture
Platforms            Immunefi · Sherlock · Code4rena · HackerOne · Bugcrowd · Intigriti
Infrastructure       Docker · PostgreSQL · Redis · GitHub Actions
```

---

## Contact

- **Security disclosures:** Responsible disclosure via official program channels
- **Consulting & audits:** abdulwahed.sweden@gmail.com
- **LinkedIn:** [abdulwahed-mansour](https://linkedin.com/in/abdulwahed-mansour)

*Open to: Protocol audits · Security consulting · DeFi security research · Account abstraction engineering*
