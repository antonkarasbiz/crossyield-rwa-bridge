# CrossYield

Cross-chain RWA yield optimizer. Tokenized real-world assets are deposited on Ethereum, bridged with Wormhole, and routed into Solana DeFi vaults with automated harvest.

## Overview

CrossYield connects two problems that usually sit in different stacks: RWA capital that originates on Ethereum, and high-throughput yield venues on Solana. The vault prices deposits from an on-chain NAV feed, then moves value across chains so harvest and compounding can run on Solana programs.

## Flow

```text
Tokenized RWA (Ethereum)
        │
        ▼
EVM vault + Chainlink NAV pricing
        │
        ▼
Wormhole bridge
        │
        ▼
Solana vault program
        │
        ▼
DeFi strategy + automated harvest
```

## Capabilities

- Deposit tokenized RWAs on Ethereum
- NAV-aware vault pricing via Chainlink
- Wormhole-based cross-chain transfer
- Solana program vault for yield routing
- Automated harvest of strategy rewards

## Repository layout

```text
programs/
  crossyield-vault/     Solana vault program
```

## Tech stack

- Rust / Solana programs
- Ethereum vault integration
- Chainlink NAV feeds
- Wormhole messaging and bridging

## Getting started

```bash
# From the Solana program package
cd programs/crossyield-vault
# Build with the Solana / Anchor toolchain installed on the host
```

Program source: [`programs/crossyield-vault/src/lib.rs`](programs/crossyield-vault/src/lib.rs)

## Related work

- [Paradex_Blockchain-web3](https://github.com/antonkarasbiz/Paradex_Blockchain-web3)
- [program-examples](https://github.com/antonkarasbiz/program-examples)
- [portfolio](https://github.com/antonkarasbiz/portfolio)

## Maintainer

[Anton Karas](https://github.com/antonkarasbiz) — full-stack, blockchain, and AI engineering.
