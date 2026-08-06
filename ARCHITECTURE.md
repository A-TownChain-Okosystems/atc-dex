# Architecture Specification — atc-dex

## Overview
`atc-dex` is designed as a core module in **L3 — DeFi** of the A-TownChain architecture.

## Repository Metadata
- **Repository Name**: `atc-dex`
- **Title**: Decentralized Exchange Engine
- **Layer**: L3 — DeFi
- **Sprint**: 2.5
- **ATC Standard**: ATC-88
- **Primary Specification**: Decentralized Exchange — AMM, Liquidity Pools, Swap, Price Oracle

## Directory Structure

```text
atc-dex/
├── amm/
│   └── amm.atc
├── pool/
│   └── pool_manager.atc
├── swap/
│   └── swap_router.atc
├── oracle/
│   └── price_oracle.atc
├── orders/
│   └── limit_orders.atc
├── fees/
│   └── dex_fees.atc
├── README.md
├── ARCHITECTURE.md
├── COMPONENT_PLAN.md
├── FILE_REGISTER.md
├── STATUS.md
├── ROADMAP.md
├── CHANGELOG.md
├── .gitignore
└── LICENSE
```

## Component Architecture Table

| Directory | File | Module Name | Primary Responsibility |
| --- | --- | --- | --- |
| `amm/` | `amm.atc` | `amm` | Automated Market Maker — Constant product, liquidity pools, swap |
| `pool/` | `pool_manager.atc` | `pool_manager` | Liquidity Pool Management — Create, add/remove liquidity |
| `swap/` | `swap_router.atc` | `swap_router` | Swap Router — Best route across pools, multi-hop |
| `oracle/` | `price_oracle.atc` | `price_oracle` | Price Oracle — TWAP, spot price, manipulation resistance |
| `orders/` | `limit_orders.atc` | `limit_orders` | Limit Orders — On-chain order book, fill logic |
| `fees/` | `dex_fees.atc` | `dex_fees` | DEX Fees — Swap fee, protocol fee, LP rewards distribution |
