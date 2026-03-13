<div align="center">

# Abdulwahed Mansour

**Smart Contract Security Researcher · Rust Systems Engineer · Protocol Architect**

[![Location](https://img.shields.io/badge/Stockholm-Sweden-0F62FE?style=flat-square)](https://github.com/abdulwahed-sweden)
[![Email](https://img.shields.io/badge/Email-abdulwahed.sweden%40gmail.com-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:abdulwahed.sweden@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-abdulwahed--mansour-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/in/abdulwahed-mansour)

</div>

---

Independent security researcher and protocol engineer specializing in DeFi vulnerabilities, ERC-4337 account abstraction, and smart contract auditing. I combine rigorous economic modeling with systems-level Rust engineering — building property-based fuzzers, formal invariant proofs, and exploit simulators to find what static analyzers miss.

Currently focused on: **intent-based account abstraction**, **liquidation mechanism exploits**, **ZK credential systems**, **Asymmetric Deficit Socialization (ADS)** in lending protocols, and **Shariah-compliant DeFi infrastructure**.

---

## Flagship Projects

<table>
<tr>
<td width="50%" valign="top">

### [`huntkey`](https://github.com/abdulwahed-sweden/huntkey)
**Intent-Based Sovereign Smart Account Protocol**

ERC-4337 Account Abstraction with a 4-layer defense-in-depth execution model. The master key never touches the network — HKDF-derived ephemeral session keys handle constrained operations through 15 on-chain validation checks.

`Rust` `Solidity` `ERC-4337` `EIP-712` `ZK Claims` `126 tests`

</td>
<td width="50%" valign="top">

### [`sunna-protocol`](https://github.com/abdulwahed-sweden/sunna-protocol)
**Shariah-Compliant DeFi Infrastructure**

ERC-4626 vault with Mudaraba profit-loss sharing, JHD effort tracking, and constitutional solvency invariants enforced at the contract level. Designed for halal financial infrastructure on EVM.

`Solidity` `Foundry` `OpenZeppelin 5.0` `ERC-4626`

</td>
</tr>
<tr>
<td width="50%" valign="top">

### [`fluid-dex-v2-security-review`](https://github.com/abdulwahed-sweden/fluid-dex-v2-security-review)
**Independent Security Audit (Sherlock Contest)**

Formal review of Instadapp's Fluid DEX V2. Built a Python-native exploit engine with 1:1 Solidity replicas, automated economic fuzzing via Hypothesis, and 198 property-based tests. 3 confirmed findings.

`Python` `Hypothesis` `DeFi` `Exploit Modeling`

</td>
<td width="50%" valign="top">

### [`amend`](https://github.com/abdulwahed-sweden/amend)
**Multi-Chain DeFi Vault Protocol**

DeFi vault protocol with formal invariant verification and transparent operations. Multi-chain architecture with per-transition invariant enforcement and trace-aware verification.

`Solidity` `Foundry` `Invariant Testing` `Multi-Chain`

</td>
</tr>
<tr>
<td width="50%" valign="top">

### [`Bitcoin-Sentinel`](https://github.com/abdulwahed-sweden/Bitcoin-Sentinel)
**Bitcoin Chain Monitoring & Analysis**

Real-time Bitcoin chain monitoring system with alerting, anomaly detection, and transaction analysis. Built in Rust for high-throughput processing.

`Rust` `Bitcoin` `Monitoring` `Async`

</td>
<td width="50%" valign="top">

### [`polaris-chronos`](https://github.com/abdulwahed-sweden/polaris-chronos)
**Universal Prayer Time Engine**

High-latitude prayer time calculations using adaptive projection and angular solar dynamics. Solves Polar Night and Midnight Sun edge cases that break conventional algorithms.

`Rust` `Astronomy` `High-Performance` `Adaptive Projection`

</td>
</tr>
</table>

---

## Security Research

### Fluid DEX V2 — Independent Audit (Sherlock Contest)

Formal security review of Instadapp's Fluid DEX V2 protocol. Built a Python-native exploit engine with 1:1 replicas of core Solidity components (BigMath, Smart Debt, fee math, liquidation), automated economic fuzzing via Hypothesis, and 198 property-based tests.

**Confirmed Findings:**

| ID | Title | Severity |
|----|-------|----------|
| #6 | Liquidation dust debt creates uncloseable positions | Low-Medium |
| #1 | Smart Debt round-trip precision loss (1-2 wei leak) | Informational |
| #7 | BigMath accounting mismatch | Informational (team-acknowledged DC#13) |

**Research domains:**
- Asymmetric Deficit Socialization (ADS) — per-transition invariant enforcement, trace-aware verification
- Liquidation mechanism exploits and dust debt analysis
- Oracle manipulation & price feed attack vectors
- Economic attack modeling with 50-decimal precision arithmetic
- Intent-based signing and ERC-4337 validation security

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
Scripting & Research Python 3.12 · FastAPI · Django · Decimal(prec=50)
Blockchain           EVM · Solana · Bitcoin · DeFi Protocol Architecture
Infrastructure       Docker · PostgreSQL · Redis · GitHub Actions
```

---

## Contact

- **Security disclosures:** Responsible disclosure via official program channels
- **Consulting & audits:** abdulwahed.sweden@gmail.com
- **LinkedIn:** [abdulwahed-mansour](https://linkedin.com/in/abdulwahed-mansour)

*Open to: Protocol audits · Security consulting · DeFi security research roles · Account abstraction engineering*
