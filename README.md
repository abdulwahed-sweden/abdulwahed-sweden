```
Security researcher. Protocol architect.
I find breaks before they cost millions.
38 projects · 208,000 lines · 5,700 tests
```

---

### What I Build

| Blockchain Security | Forensics & Intelligence | Protocol Architecture |
|:-------------------:|:------------------------:|:---------------------:|
| Smart contract auditing | On-chain crime tracing | DeFi vaults & lending |
| Oracle manipulation defense | MITRE ATT&CK mapping | ERC-4337 account abstraction |
| MEV research & mitigation | AML tooling & mempool analysis | Islamic finance primitives |

---

### Selected Work

**[huntkey](https://github.com/abdulwahed-sweden/huntkey)** `Rust` `Solidity`
Policy-enforced identity protocol combining ERC-4337 with a 4-layer defense model. Session keys are HKDF-derived, single-use, and chain-isolated — the master key never touches the network. 126 tests across Rust and Solidity.
`erc-4337` `eip-712` `zk-claims`

**[Bitcoin-Sentinel](https://github.com/abdulwahed-sweden/Bitcoin-Sentinel)** `Rust` `Python`
Blockchain forensics platform for tracing criminal fund flows across Bitcoin and Ethereum. Integrates live mempool interception, MITRE ATT&CK tactic mapping, and a built-in threat intelligence database. Competes with Chainalysis at open-source cost.
`blockchain-forensics` `mitre-attack` `aml`

**[fluid-tick-drift-guard](https://github.com/abdulwahed-sweden/fluid-tick-drift-guard)** `Solidity`
Solidity library blocking Uniswap V3 tick drift oracle manipulation attacks. Dual-layer defense using EIP-1153 transient storage (per-transaction) and permanent storage (per-block). Proven on a $50M mainnet fork simulation.
`eip-1153` `oracle-security` `flash-loan-defense`

**[amend](https://github.com/abdulwahed-sweden/amend)** `Solidity` `Rust` `Python`
Multi-chain DeFi vault protocol with 1,630 tests across EVM and Solana. Introduces EthicsGuard and FairFeeGuard — smart contracts that encode ethical constraints as on-chain invariants that governance cannot override.
`erc-4626` `multi-chain` `anchor`

**[sunna-protocol](https://github.com/abdulwahed-sweden/sunna-protocol)** `Solidity`
Shariah-compliant DeFi protocol built around the ADS vulnerability class I discovered and formalized. First protocol to implement on-chain JHD effort measurement and constitutional governance boundaries that no token vote can override.
`islamic-finance` `invariant-enforcement` `ads-vulnerability`

**[polaris-chronos](https://github.com/abdulwahed-sweden/polaris-chronos)** `Rust`
Islamic astronomical prayer time engine solving the unsolved problem of prayer calculation in polar regions. The Polaris Protocol handles extreme latitudes where standard algorithms break. Deployed on Hugging Face Spaces.
`astronomy` `polar-regions` `hugging-face`

---

### Research & Findings

- **ADS (Asymmetric Deficit Socialization)** — Vulnerability class I discovered affecting Aave V4, Morpho Blue, and Curve crvUSD. ~$98.6M phantom yield exposure across protocols that extract fees during unrealized loss periods.
- **Fluid DEX V2** — Oracle TWAP bypass and Chainlink staleness findings via Sherlock contest. 3 confirmed findings including liquidation dust debt creating uncloseable positions.
- **Moonwell/Mamo** — SlippagePriceChecker vulnerability upgraded to High severity.
- **Bybit Hack (DELTA STRIKE)** — Blockchain forensics analysis of $1.5B theft. 682 transactions, 42,479 addresses mapped, Lazarus Group attribution with THORChain/Chainflip bridge tracing.

---

### Stack

```
Rust (2024 edition) · Solidity 0.8+ · Python · TypeScript
Foundry · Anchor · ERC-4337 · Immunefi · Sherlock · Code4rena
```

---

<sub>abdulwahed.sweden@gmail.com · [LinkedIn](https://linkedin.com/in/abdulwahed-mansour)</sub>
