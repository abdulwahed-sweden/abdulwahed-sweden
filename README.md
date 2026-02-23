<div align="center">

# Abdulwahed Mansour

**Smart Contract Security Researcher · Rust Systems Engineer · DeFi Protocol Specialist**

[![Location](https://img.shields.io/badge/Stockholm-Sweden-0F62FE?style=flat-square)](https://github.com/abdulwahed-sweden)
[![Email](https://img.shields.io/badge/Email-abdulwahed.sweden%40gmail.com-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:abdulwahed.sweden@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-abdulwahed--mansour-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/in/abdulwahed-mansour)

</div>

---

Independent security researcher specializing in DeFi protocol vulnerabilities and smart contract auditing. I combine rigorous economic modeling with systems-level Rust engineering — building property-based fuzzers, formal invariant proofs, and exploit simulators to find what static analyzers miss.

Currently focused on: **liquidation mechanism exploits**, **oracle manipulation**, **Asymmetric Deficit Socialization (ADS)** in lending protocols, and **Shariah-compliant DeFi infrastructure**.

---

## Security Research

### Fluid DEX V2 — Independent Audit (Sherlock Contest)

Formal security review of Instadapp's Fluid DEX V2 protocol. Built a Python-native exploit engine with 1:1 replicas of core Solidity components (BigMath, Smart Debt, fee math, liquidation), automated economic fuzzing via Hypothesis, and 198 property-based tests.

**Confirmed Findings:**

| ID | Title | Severity |
|----|-------|----------|
| #6 | Liquidation dust debt creates uncloseable positions | Low–Medium |
| #1 | Smart Debt round-trip precision loss (1–2 wei leak) | Informational |
| #7 | BigMath accounting mismatch | Informational (team-acknowledged DC#13) |

→ [`fluid-dex-v2-security-review`](https://github.com/abdulwahed-sweden/fluid-dex-v2-security-review)

### sunna-protocol — Shariah-Compliant DeFi Infrastructure

ERC-4626-based vault with Mudaraba profit-loss sharing, JHD effort tracking, and constitutional solvency invariants enforced at the contract level. Designed for halal financial infrastructure on EVM.

→ [`sunna-protocol`](https://github.com/abdulwahed-sweden/sunna-protocol) · Solidity · Foundry · OpenZeppelin 5.0

**Research domains:**
- Asymmetric Deficit Socialization (ADS) — per-transition invariant enforcement, trace-aware verification
- Liquidation mechanism exploits and dust debt analysis
- Oracle manipulation & price feed attack vectors
- Economic attack modeling with 50-decimal precision arithmetic

---

## Engineering

**Rust**
```
Bitcoin-Sentinel    →  Bitcoin chain monitoring, alerting, and analysis system
polaris-chronos     →  High-latitude prayer time engine — Polar Night / Midnight Sun adaptive projection
chthonic            →  Modular async penetration testing framework with session management
axum-rust           →  Production web app — dark/light themes, RTL/LTR internationalization
deepseek-rust       →  Async Rust client library for DeepSeek AI API (type-safe, builder pattern)
rust-scraper-pro    →  Production-grade web scraping with AI integration and processing pipelines
weather_api_rust    →  High-performance REST API with MCP protocol integration for Claude Code
```

**Smart Contracts**
```
sunna-protocol      →  Shariah-compliant DeFi vault (Foundry, Solidity 0.8.20)
amend-protocol      →  ERC-4626 vault + Engine architecture (archived → private monorepo)
```

**Web & AI**
```
BookFlow            →  FastAPI + Vue.js appointment booking system with JWT auth
deepseek-ai-chatbot →  Next.js + Vercel AI SDK multi-provider chatbot with chat persistence
docker-mcp-postgres →  MCP server with Docker + PostgreSQL for AI agent integration
```

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
Smart Contracts      Solidity · EVM Internals · OpenZeppelin 5.0
Systems Engineering  Rust · Tokio · Axum · async-std
Scripting & Research Python 3.12 · FastAPI · Django · Decimal(prec=50)
Blockchain           EVM · Solana · DeFi Protocol Architecture
Infrastructure       Docker · PostgreSQL · Redis · GitHub Actions
```

---

## Contact

- **Security disclosures:** Responsible disclosure via official program channels
- **Consulting & audits:** abdulwahed.sweden@gmail.com
- **LinkedIn:** [abdulwahed-mansour](https://linkedin.com/in/abdulwahed-mansour)

*Open to: Protocol audits · Security consulting · DeFi security research roles*
