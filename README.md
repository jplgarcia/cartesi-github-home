<a href="https://cartesi.io/">
  <img src="https://avatars.githubusercontent.com/u/37696266?s=200&v=4" alt="Cartesi logo" width="80" height="80">
</a>

# Cartesi

Cartesi is an open-source framework for building application-specific rollups on Ethereum and other EVM-compatible chains.
Its Linux execution environment gives applications access to a filesystem, memory, and programming languages and libraries available for RISC-V Linux, with computation performed off-chain.

[Build your first application](https://docs.cartesi.io/get-started/quickstart/) or [explore the documentation](https://docs.cartesi.io/).

## Core technology

**[Cartesi Machine](https://github.com/cartesi/machine-emulator)** is a deterministic RISC-V emulator that runs Linux.
It provides a reproducible execution environment for applications built with languages and libraries available for RISC-V Linux.
Independent validators can reproduce computations and check their results.

**[Cartesi Rollups](https://docs.cartesi.io/cartesi-rollups/2.0/getting-started/architecture/)** combines the Machine, smart contracts, and the Cartesi Rollups Node into an application-specific rollup.
Each application has its own Machine and state.
The node reads inputs recorded on the base chain, executes the application off-chain, and submits claims about the results for on-chain settlement.

**[Dave](https://github.com/cartesi/dave)** is Cartesi's permissionless fraud-proof system.
Applications using PRT (Permissionless Refereed Tournaments) allow anyone to validate execution and dispute incorrect results through an on-chain Machine verifier.

**Zero-knowledge (ZK) research** explores proofs of Cartesi Machine state transitions as an additional approach to verifiable computation.

## Explore and contribute

Cartesi is developed as an open-source public good, with infrastructure available for anyone to use, inspect, and contribute to.

- [Cartesi Machine](https://github.com/cartesi/machine-emulator): explore the execution environment and use it independently.
- [Rollups Node](https://github.com/cartesi/rollups-node): run the node software connecting on-chain inputs, Machine execution, and application clients.
- [Rollups Contracts](https://github.com/cartesi/rollups-contracts): explore the smart contracts for application inputs and settlement.
- [CLI](https://github.com/cartesi/cli): create, build, and run an application.
- [Engineering map](ENGINEERING_MAP.md): find repositories, component status, and dependencies.
- [Developer community](https://discord.gg/cartesi): ask questions and discuss what you are building.

Contributions are welcome through each repository's contribution guidelines.
Licenses vary by component: the [Machine emulator](https://github.com/cartesi/machine-emulator/blob/main/COPYING) uses LGPL-3.0; [Dave](https://github.com/cartesi/dave/blob/main/LICENSE), [Rollups Contracts](https://github.com/cartesi/rollups-contracts/blob/main/LICENSE), and the [CLI](https://github.com/cartesi/cli/blob/prerelease/v2-alpha/LICENSE) use Apache-2.0.
Cartesi-authored [Rollups Node code](https://github.com/cartesi/rollups-node/blob/main/LICENSE) uses Apache-2.0 or compatible permissive licenses; its [README](https://github.com/cartesi/rollups-node#license) also documents GPL-3.0 requirements for the combined component due to dependencies.
See each repository for its full license terms and dependency notices.
