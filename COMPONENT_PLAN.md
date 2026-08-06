# Component Plan — atc-dex

This document details the components, primary data structures, and core functions implemented in `atc-dex`.

## Core Component Specification

### 1. Automated Market Maker (`amm/amm.atc`)
- **Module**: `amm`
- **ATC Standard**: `ATC-88`
- **Description**: Constant product, liquidity pools, swap
- **Key Data Structure**: `PoolPair`
- **Key Function**: `calculate_swap_output()` — Calculates output amount for swap based on constant product formula (x * y = k)

### 1. Liquidity Pool Management (`pool/pool_manager.atc`)
- **Module**: `pool_manager`
- **ATC Standard**: `ATC-88`
- **Description**: Create, add/remove liquidity
- **Key Data Structure**: `PoolPosition`
- **Key Function**: `add_liquidity()` — Adds tokens to liquidity pool and mints LP tokens

### 1. Swap Router (`swap/swap_router.atc`)
- **Module**: `swap_router`
- **ATC Standard**: `ATC-88`
- **Description**: Best route across pools, multi-hop
- **Key Data Structure**: `SwapPath`
- **Key Function**: `find_best_route()` — Finds optimal route across liquidity pools for minimal slippage

### 1. Price Oracle (`oracle/price_oracle.atc`)
- **Module**: `price_oracle`
- **ATC Standard**: `ATC-88`
- **Description**: TWAP, spot price, manipulation resistance
- **Key Data Structure**: `PriceObservation`
- **Key Function**: `update_twap()` — Updates Time-Weighted Average Price accumulator

### 1. Limit Orders (`orders/limit_orders.atc`)
- **Module**: `limit_orders`
- **ATC Standard**: `ATC-88`
- **Description**: On-chain order book, fill logic
- **Key Data Structure**: `LimitOrder`
- **Key Function**: `fill_order()` — Executes matching limit order when target price is reached

### 1. DEX Fees (`fees/dex_fees.atc`)
- **Module**: `dex_fees`
- **ATC Standard**: `ATC-88`
- **Description**: Swap fee, protocol fee, LP rewards distribution
- **Key Data Structure**: `FeeStructure`
- **Key Function**: `distribute_fees()` — Splits collected trading fees between LPs and protocol treasury

