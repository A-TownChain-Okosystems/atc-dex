# atc-dex — Decentralized Exchange Engine

Decentralized Exchange — AMM, Liquidity Pools, Swap, Price Oracle

## Quick Facts

| Fact | Value |
| --- | --- |
| Repo | `atc-dex` |
| Organization | A-TownChain-Okosystems |
| Layer | `L3 — DeFi` |
| Sprint | `2.5` |
| ATC Standard | `ATC-88` |
| Language | ATCLang v0.3 |
| Status | Active Development |
| License | MIT |

## Overview

The `atc-dex` module forms a core pillar of the A-TownChain ecosystem under specification **ATC-88**. It provides full-featured ATCLang implementation for key infrastructure capabilities across `L3 — DeFi`.

## Modules Summary

- **`amm/amm.atc`**: Automated Market Maker — Constant product, liquidity pools, swap
- **`pool/pool_manager.atc`**: Liquidity Pool Management — Create, add/remove liquidity
- **`swap/swap_router.atc`**: Swap Router — Best route across pools, multi-hop
- **`oracle/price_oracle.atc`**: Price Oracle — TWAP, spot price, manipulation resistance
- **`orders/limit_orders.atc`**: Limit Orders — On-chain order book, fill logic
- **`fees/dex_fees.atc`**: DEX Fees — Swap fee, protocol fee, LP rewards distribution

## Getting Started

1. Ensure the ATCLang toolchain v0.3+ is installed.
2. Clone this repository into your workspace.
3. Import modules into your ATCLang entrypoints.

## License

This repository is licensed under the [MIT License](LICENSE).
