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

**[Cartesi Rollups](https://docs.cartesi.io/cartesi-rollups/2.0/getting-started/architecture/)** combines the Machine, smart contracts, and the Cartesi Rollups Node into an SDK for application-specific rollups.
Each application has its own Machine and state.
The node reads inputs recorded on the base chain, executes the application off-chain, and submits claims about the results for on-chain settlement.
Deployment and node operation are permissionless: anyone can deploy an application and run a node.

**[Dave](https://github.com/cartesi/dave)** is Cartesi's permissionless fraud-proof system.
Applications using it allow anyone to validate execution and dispute incorrect results through an on-chain Machine verifier.
Cartesi is also researching zero-knowledge (ZK) proofs of Machine state transitions as another approach to verifying computation.

## Explore and contribute

Cartesi is developed as an open-source public good, with infrastructure available for anyone to use, inspect, and contribute to.

- [Cartesi Machine](https://github.com/cartesi/machine-emulator): explore the execution environment and use it independently.
- [Rollups Node](https://github.com/cartesi/rollups-node): run the node software connecting on-chain inputs, Machine execution, and application clients.
- [Rollups Contracts](https://github.com/cartesi/rollups-contracts): explore the smart contracts for application inputs and settlement.
- [CLI](https://github.com/cartesi/cli): create, build, and run an application.
- [Engineering map](ENGINEERING_MAP.md): find repositories, component status, and dependencies.
- [Developer community](https://discord.gg/cartesi): ask questions and discuss what you are building.

Contributions are welcome through each repository's contribution guidelines.
Licenses vary by component: the Cartesi Machine uses LGPL-3.0; Dave, Rollups Contracts, Rollups Node, and the CLI use Apache-2.0.
See each repository for its full license terms and dependency notices.
